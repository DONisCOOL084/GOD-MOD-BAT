@echo off
color 0a
title [ GODMODE INSTALLER RAW VERSION ]

:menu
cls
echo ==============================
echo   GODMODE INSTALLER - CHOOSE LOCATION
echo ==============================
echo.
echo [1] Desktop
echo [2] Documents
echo [3] Downloads
echo [4] Custom Path
echo [5] Same Folder as This Script
echo [6] Cancel
echo.
set /p choice=Enter your choice (1-6): 

if "%choice%"=="1" set location=%UserProfile%\Desktop
if "%choice%"=="2" set location=%UserProfile%\Documents
if "%choice%"=="3" set location=%UserProfile%\Downloads
if "%choice%"=="4" goto custom
if "%choice%"=="5" set location=%~dp0
if "%choice%"=="6" exit
if not defined location goto invalid

:install
cls
echo Installing GodMode to: %location%
mkdir "%location%\GODMODE.{ED7BA470-8E54-465E-825C-99712043E01C}"
echo.
echo ✅ GodMode folder created at: %location%
pause
exit

:custom
cls
echo Enter full custom path where you want to install GodMode:
set /p location=Path: 
if not exist "%location%" (
    echo ❌ That path does not exist.
    pause
    goto menu
)
goto install

:invalid
echo ❌ Invalid choice. Try again.
pause
goto menu
