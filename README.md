# lan-file-transfer

局域网里的多文件传输。服务端按策略把文件分给节点，发送端按区间推数据，接收端收齐并画出进度。

写于 2020 年。仓库原名 `easyFileTans`，少了一个 r，这里改成能看懂的名字。

## 里面有什么

- `MFCTServer`：交互端口、传输端口，以及可替换的 `IFileDistributeStrategy`
- `Sender` / `Receiver`：按资源区间发送和接收，接收端用线程池拉数据
- `Resource`、`ResourceFile`、`OffsetLen`：描述要传的文件和还没收到的片段
- `ProgressBar`：传输进度

源码在 `多文件局域网传输/src`，包名 `com.mec.mfct`。目录是当时的 Eclipse 工程。传输层用到同系列的 `MyRmi.jar`（[mini-rmi](https://github.com/ailan-aoi/mini-rmi)）。

## 状态

学习代码，源码按最初上传的样子保留。旧地址 `easyFileTans` 会重定向到这里。
