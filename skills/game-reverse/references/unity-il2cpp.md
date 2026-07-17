# Unity IL2CPP 最小路径

1. 取 `GameAssembly.dll` + `global-metadata.dat`  
2. Il2CppDumper → `DummyDll` + `script.json`  
3. IDA 加载 GameAssembly，导入 script 或手动映射 RVA  
4. 关键逻辑：登录、支付校验、反篡改  
5. Frida 验证  

Mono：直接 dnSpyEx `Assembly-CSharp.dll`。