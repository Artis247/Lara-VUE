Решенная проблемка (напоминалка): composer create-project --prefer-dist lara/lara ...

1. php --ini
2. This C:\WINDOWS here is a hoax. When I looked in the php installation directory, I found out there is NO php.ini. There are two files php.ini-development and php.ini-production. Just rename one to php.ini
3. Afterwards, open the php.ini file and uncomment the following line ;extension_dir = "ext" should be

extension_dir = "ext" 

4. Enable extensions
Then uncomment the extensions the same way. The following are usually required. (But please find out what you need from the messages you see from composer commands)

extension=fileinfo <br>
extension=gd2 <br>
extension=mbstring <br>
extension=openssl <br>
