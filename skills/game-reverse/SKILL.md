---
name: game-reverse
description: Use for authorized game client reverse engineering including Unity IL2CPP/Mono, Unreal, anti-cheat surfaces, and memory analysis for security research.
---

# Game Client Reverse Engineering

## ACTION REQUIRED（读完后立刻执行）

1. `NOW`: 读取 `../field-journal/precedent-reverse.md`
2. `NOW`: 确认授权（仅自有/授权样本；禁止未授权外挂开发指导用于破坏）
3. `NOW`: 识别引擎（Unity / UE / 自研）
4. `NEXT`: tool-index；Il2CppDumper 等手动
5. `ACT`: 引擎分诊 → 结构转储 → 逻辑还原

## 适用场景

- Unity Mono / IL2CPP 符号与字符串恢复
- Unreal 对象与协议
- 反作弊表面研究（安全评估语境）
- 内存结构分析（CE）服务漏洞研究或加固验证
- 游戏相关协议 → 联合 `protocol-reverse/`

## 工作流

### 1. 引擎识别

```text
□ GameAssembly.dll + global-metadata.dat → IL2CPP
□ Assembly-CSharp.dll → Mono
□ UE4/5：Shipping exe + pak
```

### 2. Unity IL2CPP

```text
□ Il2CppDumper 生成 DummyDll + script.json
□ 用 dnSpyEx 看 DummyDll 签名；用 IDA/Ghidra 看原生实现
□ Frida hook 关键导出 / 方法 RVA
```

### 3. 协议与校验

```text
□ 抓包 + 客户端序列化函数
□ 反作弊模块单独样本分析 → malware 方法学 + ida
```

## 工具链

| 工具 | 用途 |
|------|------|
| Il2CppDumper | IL2CPP 还原 |
| dnSpyEx | DummyDll / Mono |
| IDA / Ghidra | 原生 |
| Frida | 运行时 |
| AssetStudio | 资源 |

## 参考

- `references/unity-il2cpp.md`
- `field-journal/seed-014_unity-il2cpp-reverse.md`
- `../dotnet-reverse/` `../protocol-reverse/` `../ida-reverse/`

## 路由上下文

**上游**: MASTER R28  
**下游**: 协议 `protocol-reverse`；加固 so `ida-reverse`

## 任务完成自检

- [ ] 是否正确识别引擎？
- [ ] 是否有地址/符号级结论？
- [ ] 授权与用途是否合规？
- [ ] Checklist？