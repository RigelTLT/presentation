https://css-tricks.com/getting-started-with-the-file-system-access-api/
The File System Access API is a web API that allows read and write access to a user’s local files. It unlocks new capabilities to build powerful web applications, such as text editors or IDEs, image editing tools, improved import/export, all in the frontend.

Reading files with the File System Access API
Before diving into the code required to read a file from the user’s system, an important detail to keep in mind is that calling the File System Access API needs to be done by a user gesture, in a secure context.

------------------------------
https://developer.mozilla.org/en-US/docs/Web/API/FileSystem
The File and Directory Entries API interface FileSystem is used to represent a file system. These objects can be obtained from the filesystem property on any file system entry. Some browsers offer additional APIs to create and manage file systems, such as Chrome's requestFileSystem() method.

This interface will not grant you access to the users filesystem. Instead you will have a "virtual drive" within the browser sandbox. If you want to gain access to the users filesystem you need to invoke the user by eg. installing a Chrome extension. 
Basic concepts

There are two ways to get access to a FileSystem object:

You can directly ask for one representing a sandboxed file system created just for your web app directly by calling window.requestFileSystem(). If that call is successful, it executes a callback handler, which receives as a parameter a FileSystem object describing the file system.
You can get it from a file system entry object, through its filesystem property.

------------------------------------------------------
https://habr.com/ru/post/112286/
В качестве введения

С помощью FileSystem API и File API веб приложение может создавать, читать, просматривать и записывать файлы находящиеся в области пользовательской «песочницы».

Описание API разбито на следующие секции:
Чтение и управление файлами: File/Blob, FileList, FileReader
Создание и запись: BlobBuilder, FileWriter
Работа с директориями и права доступа: DirectoryReader, FileEntry/DirectoryEntry, LocalFileSystem
Пара слов об объектах, с которыми предстоит работать:
File — собственно файл; позволяет получить такую доступную только для чтения информацию, как имя, размер, mimetype и прочее.
FileList — «массив» объектов File.
Blob — сущность, позволяющая разбирать файл по байтам.

------------------------------------------------------
https://web.dev/file-system-access/
The File System Access API is currently supported on most Chromium browsers on Windows, macOS, ChromeOS, and Linux. 
------------------------------------------------------
https://en.wikipedia.org/wiki/File_system_API