---
title: Registering a Type Library
description: Demonstrates how to register a type library.
ms.assetid: 'ef1a720c-dece-4fdb-bbb1-66ffb33a5157'
---

# Registering a Type Library

Tools and applications that expose type information must register the information so that it is available to type browsers and programming tools. The correct registration entries for a type library can be generated by calling the [**RegisterTypeLib**](registertypelib.md) function on the type library. You can then use Regedit.exe to write the registration entries to a text file from the system registration database.

The following information is registered for a type library:


```C++
\TypeLib\{libUUID}
\TypeLib\{libUUID}\major.minor = human_readable_string 
\TypeLib\{libUUID}\major.minor\HELPDIR = [helpfile_path]
\TypeLib\{libUUID}\major.minor\Flags = typelib_flags
\TypeLib\{libUUID}\major.minor\lcid\platform = localized_typelib_filename
```



## Parameters

<dl> <dt>

<span id="libUUID"></span><span id="libuuid"></span><span id="LIBUUID"></span>*libUUID*
</dt> <dd>

The universally unique ID of the type library.

</dd> <dt>

<span id="major.minor"></span><span id="MAJOR.MINOR"></span>*major*.*minor*
</dt> <dd>

The two-part version number of the type library. If only the minor version number increases, all the features of the previous type library are supported in a compatible way. If the major version number changes, code that compiled against the type library must be recompiled. The version number of the type library may differ from the version number of the application.

</dd> <dt>

<span id="human_readable_string"></span><span id="HUMAN_READABLE_STRING"></span>*human\_readable\_string*
</dt> <dd>

A string that describes the type library to users. The recommended maximum length is 40 characters.

</dd> <dt>

<span id="helpfile_path"></span><span id="HELPFILE_PATH"></span>*helpfile\_path*
</dt> <dd>

The directory where the Help file for the types in the type library is located. If the application supports type libraries for multiple languages, the libraries may refer to different file names in the Help file directory.

</dd> <dt>

<span id="typelib_flags"></span><span id="TYPELIB_FLAGS"></span>*typelib\_flags*
</dt> <dd>

The hexadecimal representation of the type library flags for this type library. These are the values of the LIBFLAGS enumeration, and are the same flags specified in the *uLibFlags* parameter to [**ICreateTypeLib::SetLibFlags**](icreatetypelib-setlibflags.md). These flags cannot have leading zeros or the 0x prefix.

</dd> <dt>

<span id="lcid"></span><span id="LCID"></span>*lcid*
</dt> <dd>

The hexadecimal string representation of the locale identifier (LCID). It is one to four hexadecimal digits with no 0x prefix and no leading zeros. The LCID may have a neutral sublanguage ID.

</dd> <dt>

<span id="platform"></span><span id="PLATFORM"></span>*platform*
</dt> <dd>

The target operating system platform: 16-bit Windows, 32-bit Windows, or Apple Macintosh.

</dd> <dt>

<span id="localized_typelib_filename"></span><span id="LOCALIZED_TYPELIB_FILENAME"></span>*localized\_typelib\_filename*
</dt> <dd>

The full name of the localized type library.

</dd> </dl>

## Remarks

Using the LCID specifier, an application can explicitly register the file names of type libraries for different languages. This allows the application to find the desired language without having to open all type libraries with a given name.

For example, to find the type library for Australian English (309), the application first looks for it. If that fails, the application looks for an entry for standard English (a primary identifier of 0x09). If there is no entry for standard English, the application looks for LANG\_SYSTEM\_DEFAULT (0). For more information on locale support, see [National Language Support](https://msdn.microsoft.com/library/windows/desktop/dd319078).

## Type Library Registration Example


```C++
; Type library registration information.
HKEY_CLASSES_ROOT\TypeLib\{F37C8060-4AD5-101B-B826-00DD01103DE1}
HKEY_CLASSES_ROOT\TypeLib\{F37C8060-4AD5-101B-B826-00DD01103DE1}\2.0 = Automation Hello 2.0 Type Library.
HKEY_CLASSES_ROOT\TypeLib\{F37C8060-4AD5-101B-B826-00DD01103DE1}\2.0\HELPDIR =
; U.S. English.
HKEY_CLASSES_ROOT\TypeLib\{F37C8060-4AD5-101B-B826-00DD01103DE1}\2.0\9\win32 = hello.tlb
```



 

 



