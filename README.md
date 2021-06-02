macOS 10.15.5, Node v16.2.0

1. Run `yarn`
2. Run `yarn build`, this error should be printed:

```
#
# Fatal error in , line 0
# Check failed: result.second.
#
#
#
#FailureMessage Object: 0x700008408350
 1: 0x104ccaaae node::NodePlatform::GetStackTracePrinter()::$_3::__invoke() [/usr/local/Cellar/node/16.2.0/bin/node]
 2: 0x10551a21e V8_Fatal(char const*, ...) [/usr/local/Cellar/node/16.2.0/bin/node]
 3: 0x104ff1d25 v8::internal::GlobalBackingStoreRegistry::Register(std::__1::shared_ptr<v8::internal::BackingStore>) [/usr/local/Cellar/node/16.2.0/bin/node]
 4: 0x104db9f11 v8::ArrayBuffer::GetBackingStore() [/usr/local/Cellar/node/16.2.0/bin/node]
 5: 0x104c4e2b8 node::Buffer::Data(v8::Local<v8::Value>) [/usr/local/Cellar/node/16.2.0/bin/node]
 6: 0x1093963df EnvWrap::batchWrite(Nan::FunctionCallbackInfo<v8::Value> const&) [node_modules/lmdb-store/prebuilds/darwin-x64/node.abi93.node]
 7: 0x109397833 Nan::imp::FunctionCallbackWrapper(v8::FunctionCallbackInfo<v8::Value> const&) [node_modules/lmdb-store/prebuilds/darwin-x64/node.abi93.node]
 8: 0x104dff25e v8::internal::FunctionCallbackArguments::Call(v8::internal::CallHandlerInfo) [/usr/local/Cellar/node/16.2.0/bin/node]
 9: 0x104dfe92c v8::internal::MaybeHandle<v8::internal::Object> v8::internal::(anonymous namespace)::HandleApiCallHelper<false>(v8::internal::Isolate*, v8::internal::Handle<v8::internal::HeapObject>, v8::internal::Handle<v8::internal::HeapObject>, v8::internal::Handle<v8::internal::FunctionTemplateInfo>, v8::internal::Handle<v8::internal::Object>, v8::internal::BuiltinArguments) [/usr/local/Cellar/node/16.2.0/bin/node]
10: 0x104dfe003 v8::internal::Builtin_Impl_HandleApiCall(v8::internal::BuiltinArguments, v8::internal::Isolate*) [/usr/local/Cellar/node/16.2.0/bin/node]
11: 0x10542bb39 Builtins_CEntry_Return1_DontSaveFPRegs_ArgvOnStack_BuiltinExit [/usr/local/Cellar/node/16.2.0/bin/node]
```