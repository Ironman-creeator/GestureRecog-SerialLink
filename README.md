# GestureRecog-SerialLink
该项目将计算机视觉技术与串行通信功能相结合。它从摄像头捕获视频流，实时检测手部动作，并准确识别各种手势。识别结果不仅在视频帧上进行视觉标记，还通过串行端口发送，以便与其他外部设备或系统进行交互。它具有精确的手势识别、实时图像注释和高效的串行通信功能，适用于智能控制、人机交互、教育和娱乐场景。

项目概述 
本项目是一个综合性的应用，结合了计算机视觉技术与串口通信功能。它能够通过摄像头捕获视频流，实时检测其中的手部动作，并准确识别多种手势。识别结果不仅会直观地标注在视频画面上，还会通过串口将相关数据发送出去，以便与其他外部设备或系统进行交互。
功能特性
手势识别精准：利用 mediapipe 库，可精准定位手部在视频帧中的位置，精确分析每根手指的状态，能准确识别如单手或双手的各种常见手势组合，包括一根手指到五根手指竖起的不同情况等。
图像标注实时：根据手势识别结果，立即在视频画面上以清晰醒目的文字（如 “1_ONE”“2_TWO” 等）标注出手势信息，不影响视频观看且能有效传达识别结果。
串口通信高效：自动扫描并列出系统中可用的串口设备，可便捷地对串口进行配置（如波特率设为 115200），将手势识别结果以特定格式（如数字字符串）编码后通过串口稳定发送，确保数据传输的准确性与完整性。
应用场景
智能控制：适用于智能家居系统中对灯光、电器等设备的手势控制，也可用于工业场景下对机器人或特定设备的远程操控。
人机交互：在虚拟现实（VR）/ 增强现实（AR）体验中提供自然交互方式，或为特殊人群提供无障碍交互手段。
教育娱乐：可助力开发互动式教学软件，让教师通过手势灵活控制教学演示；也能为游戏增添新颖玩法，提升玩家的参与感。
技术亮点
先进算法保障：基于 mediapipe 的高效识别算法，配合优化的手指状态判断逻辑，实现高准确率、低延迟的手势识别，带来流畅的使用体验。
架构灵活拓展：代码结构清晰明了，易于理解与修改。方便开发者依据实际需求，轻松拓展手势种类或调整串口通信协议，以适配各类应用场景与设备。
跨平台兼容无忧：依托 Python 常用库（opencv、mediapipe、serial 等）构建，具备出色的跨平台特性，可在 Windows、Linux、MacOS 等多种操作系统上稳定运行，有效降低部署成本与难度。
快速开始
环境准备：确保已安装 Python 环境，并安装所需依赖库，如 opencv-python、mediapipe、pyserial 等。
硬件连接：将摄像头连接至计算机，并确保串口设备（如目标设备连接在 COM3 端口）已正确连接且可被识别。
运行程序：直接执行主程序脚本，程序将启动摄像头，开始手势识别与串口通信流程。在摄像头画面中展示手势，即可看到识别结果标注，同时串口数据将按设定发送。
贡献指南
欢迎开发者对本项目进行贡献。若您发现任何问题或有新的功能想法，请提交 Issue 进行讨论。如果您想提交代码修改，请遵循以下步骤：
Fork 本项目仓库。
创建您的特性分支（git checkout -b feature/your-feature）。
提交您的修改（git commit -am 'Add some feature'）。
将您的分支推送到您的远程仓库（git push origin feature/your-feature）。
提交 Pull Request，详细描述您的修改内容与目的。
注意事项
摄像头的拍摄质量与环境光线可能会对手势识别效果产生一定影响，请尽量在光线均匀、充足的环境下使用。
串口设备的配置参数（如串口号、波特率等）需根据实际连接情况准确设置，否则可能导致通信失败。
