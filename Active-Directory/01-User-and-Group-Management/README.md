# User and Group Management

## الهدف
إنشاء مستخدم داخل Active Directory وإضافته إلى مجموعة أمنية، ثم التحقق من تسجيل الحدث الأمني.

## الأدوات
- Windows Server 2022
- Active Directory Users and Computers
- Event Viewer

## الخطوات
1. إنشاء المستخدم.
2. إنشاء المجموعة الأمنية.
3. إضافة المستخدم إلى المجموعة.
4. التحقق من Event ID 4728.

## النتيجة
تمت إضافة المستخدم بنجاح، وتم تسجيل الحدث في سجل الأمان.

## الصور
![User Membership](Images/01-user-membership.png)
![Event 4728](Images/02-event-4728.png)
![Create GPO](Images/01-create-gpo.png)
![Control Panel Disabled](Images/03-control-panel-disabled.png)
