# Cocos_Protos

cocos2dx 3.17 使用的 simulator 集成了protobuf-lite 2.5.0，并且使用该版本的protobuf生成了文件Protos.pb.h和Protos.pb.cc，但是并未提供声明文件Protos.proto。导致无法在cocos2dx上集成更高版本的protobuf（c++版本），同时protobuf 2.5.0并不支持64位系统，而ios需要发布64位版本游戏。

我根据2.5.0版本的Protos.pb.h文件反推出了Protos.proto文件

注意集成新版protobuf的时候 需要移除simulator下原有的protobuf-lite 2.5.0，避免版本冲突
