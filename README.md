# MCSemaWindows
MCSema Build Windows download

For CFG Construction:
ida64.exe -S"D:\remill\mcsema\Lib\site-packages\mcsema_disass-2.0-py3.8.egg\mcsema_disass\ida7\get_cfg.py --output calc.cfg --log_file calc.log --arch amd64 --os windows --entrypoint wWinMain" calc.exe

Generate LLVM Bitcode from Exe File:
mcsema-lift-5.0.exe --os windows --arch amd64 --cfg calc.cfg --output calc.bc

Then you can use the bitcode back with clang or clang-cl on windows
