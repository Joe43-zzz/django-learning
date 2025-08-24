# Django 学习笔记（2025-08-24）

## 1. 创建虚拟环境
```powershell
python -m venv venv
venv\scripts\activate
```
- 遇到问题：PowerShell 提示无法运行 `Activate.ps1`（脚本执行被禁止）。
- 解决方法：
```powershell
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
```
- 成功激活虚拟环境。

## 2. 安装 Django
- 初始环境包：
```
pip        22.2.2
setuptools 63.2.0
```
- 安装 Django：
```powershell
pip install django
```
- 安装成功：
```
Django 5.2.5
asgiref 3.9.1
sqlparse 0.5.3
typing_extensions 4.14.1
tzdata 2025.2
```

## 3. 创建 Django 项目
```powershell
django-admin startproject demo
cd demo
```
- 确认 `manage.py` 存在。

## 4. 运行开发服务器
```powershell
python manage.py runserver
``]
- 成功启动：http://127.0.0.1:8000/
- 系统提示：有 **18 个未应用迁移**。

## 5. 创建应用
```powershell
django-admin startapp app01
```
- 注意：曾拼写错误 `manange.py`，报错文件不存在。

## 6. 应用迁移
```powershell
python manage.py migrate
```
- 成功应用所有默认迁移（auth、admin、contenttypes、sessions）。

## ✅ 今日成果
- 成功安装并配置 Django 环境。
- 新建了 Django 项目 `demo` 并运行成功。
- 数据库迁移已完成。
- 新建应用 `app01`，可用于后续开发。
