# Error Virus
Вирус, который при открытии будет **бесконечно сыпать ошибками**.![Вирус в действии](https://github.com/denis0001-dev/error-virus/blob/main/img/inaction.gif?raw=true)
# Компиляция
В [Bat to Exe Converter](https://bat-to-exe-converter-x64.en.softonic.com/) откройте [virus.bat](https://raw.githubusercontent.com/denis0001-dev/error-virus/main/virus.bat) и поставьте следующие настройки:

 - [ ] **Icon**: [error.ico](https://raw.githubusercontent.com/denis0001-dev/error-virus/main/error.ico)
 - [ ] **Working directory**: Temporary directory
 - [ ] **Exe-Format**: 32 Bit | Windows (Invisible)
 - [ ] **Overwrite**: Yes

Потом на вкладке **Embed** перетащите [virus.vbs](https://raw.githubusercontent.com/denis0001-dev/error-virus/main/virus.vbs) и нажмите Convert. Назовите **имя выходного exe-файла** и готово!

Настройки должны **получится так**:
![Главные настройки](https://github.com/denis0001-dev/error-virus/blob/main/img/mainsettings.png?raw=true)
![Настройки встаивания](https://github.com/denis0001-dev/error-virus/blob/main/img/embedsettings.png?raw=true)
# Как он работает
При запуске, вирус запускает [virus.vbs](https://raw.githubusercontent.com/denis0001-dev/error-virus/main/virus.vbs) из bat-файла, конвертированного в **exe** с помощью `wscript ./virus.vbs`.
Дальше, он запускает самого себя через `CreateObject("WScript.Shell").Run(".\\virus.vbs")` и создает **окно ошибки**:
![Окно ошибки](https://github.com/denis0001-dev/error-virus/blob/main/img/error_window.png?raw=true)
Для показа **окна ошибки** используется `hydro = msgbox("Your computer just got hacked", 0+16, "Error")`, где:
|Значение                         | Параметр | 
|---------------------------------|----------| 
|`"Your computer just got hacked"`|Описание  |
|`0+16`                           |`кнопка ОК`+`иконка ошибки` |
| `hydro`                         | Переменная, где хранится окно |
|`"Error"`                        | Заголовок
Этот код **сильно нагружает ваш ПК**, но не вредит ему. Запускайте вирус **на свой страх и риск!**
**Ему даже права администратора не нужны!**
# Как завершить этот вирус
Нажмите **Windows+R** и напишите `cmd.exe` в открывшемся диалоге. Далее запустите `taskkill /f /im wscript.exe`. Но если после этого окна с ошибками не перестанут появлятся **запустите эту команду еще раз.**
# Ссылки
[GConvert](https://www.gdgsoft.com/gconvert/download) (использовал для извлечения иконки для вируса)
[Bat to Exe Converter](https://bat-to-exe-converter-x64.en.softonic.com/) (использовано для компиляции)
