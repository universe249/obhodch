# Как выпустить обновление

1. Получить новый архив, например `Obhod-v3.6.zip`.
2. Подписать (папка `tools`, PowerShell):
   ```
   .\release.exe sign C:\путь\Obhod-v3.6.zip 3.6
   ```
   Рядом появятся `manifest.json` и `manifest.json.sig`.
3. На GitHub: **Releases → Draft a new release**.
   - Tag: `v3.6` (создать новый), Title: `Версия 3.6`.
   - В описание написать, что изменилось (покажется в программе).
   - Прикрепить три файла: `Obhod-v3.6.zip`, `manifest.json`, `manifest.json.sig`.
   - **Publish release** (не pre-release и не draft).
4. Запущенные программы увидят версию в течение нескольких часов.

Ключ `signing.key` секретный. Не выкладывать в репозиторий.
