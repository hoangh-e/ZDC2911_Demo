@echo off
setlocal enabledelayedexpansion

for %%f in (*.*) do (
    rem Bỏ qua các file đã có đuôi .txt
    if /I not "%%~xf"==".txt" (
        copy "%%f" "%%f.txt" >nul
        echo Đã tạo: %%f.txt
    )
)

echo Hoàn tất!
pause
