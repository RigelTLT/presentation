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
https://en.wikipedia.org/wiki/File_system_API

--------------------------------------------------------
https://wicg.github.io/entries-api/#filesystem
----------------------------------------------------
http://html5ru.com/filesystem-api.html