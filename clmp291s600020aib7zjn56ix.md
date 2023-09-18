---
title: "Linux File Permissions: A Simple Guide"
seoTitle: "Linux File Permissions: Easy Guide"
seoDescription: "Learn the basics of Linux file permissions in this easy-to-follow guide. Understand how to control access and secure your files effortlessly."
datePublished: Mon Sep 18 2023 15:48:13 GMT+0000 (Coordinated Universal Time)
cuid: clmp291s600020aib7zjn56ix
slug: linux-file-permissions-a-simple-guide
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1695046955648/5e93ad83-b964-41d8-8189-04b95b5d7529.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1695047197613/cddbd05d-a257-471d-8c98-98df2a218f44.png
tags: linux, hashnode, linux-for-beginners, linux-commands, file-permission

---

File permissions are an essential part of managing and maintaining a Linux system because they control the access to files and directories and ensure the security of the Linux system and the data stored in the files and directories.

As a system administrator, developer, or regular Linux user, you should know and understand how file permissions work. This article will explore the dos and don’ts of Linux file permissions and how to manage them.

### Understanding File Permissions

Linux has a permission system based on three key attributes:

* **Read access**: This is symbolized as '*r'; it* gives the user access to read the file.
    
* **Write access**: This is symbolized as '*w'; it* gives the user access to write or modify the file.
    
* **Execute access**: This is symbolized as '*x'*; it gives the user access to execute a command on the file.
    

These permissions are usually assigned to three entities on the Linux file system.

* **Owner**: Signifies the user who created the file and is usually your default Linux user.
    
* **Group**: A group of users with shared ownership or access to the file.
    
* **Others**: This user didn’t create the file or isn’t in the group with access. They could have a specific permission attribute access to the file.
    

### Granting File Permissions

In Linux, granting file permissions can be tricky. The *chmod* command is the tool for managing file permissions.

To grant specific file permission to a user or group, specify the user (u) or group (g), followed by the permission attribute and the file name.

The syntax is as follows:

`chmod [entity + permissions] [file]`

The command below will set write permission for a user group of the file file.txt. The current owner of the file will still have read and write permission.

```bash
chmod g+w file.txt
```

The command below sets execution permission to the owner of the file file.txt. The other permissions won’t be tampered with.

```bash
chmod u+x file.txt
```

The command below will add read permission to the other group entity for the file file.txt. The owner and user group will still have read, write, and execution permission.

```bash
chmod o+r file.txt
```

You can also copy file permissions from an owner to a user group. You can do this by targeting a particular user of the user group.

```bash
chmod g=u file.txt
```

This command above copies the owner user permissions(r,w,x) to the user group so every user has the same permission access as the owner user.

The output of all these commands would result in this:

![](https://lh5.googleusercontent.com/5OuLjViHOdqMvWIOs5Camwbv7hCv_BbEY-2eCV0sOHH8oqN5tYKxg12LmhiZzLwqhmGdLUUuhQLElSOI8YGUTwDcpIojW13uMNGp4w_q_y1nsiD7sCMsVQZ_c7hGf9Tn3BmGJsZU45M6mk7JeSxi62eUCgwnIpuUyXH-rl-EM_U3f1L1HTZCMbfsr607ig align="left")

### Granting permissions using number notation

You can grant permissions using number notations. The permission access is assigned a value:

* Number 4 for read permission.
    
* Number 2 for write permission.
    
* Number 1 for execute permission.
    

To grant an entity-specific permission, define the value and the file name.

```bash
chmod 431 file.txt
```

This command gives the file owner read-only access, the user group writes and executes access, and the other group only executes access.

The file permission would look like this:

![](https://lh4.googleusercontent.com/5tZU9-edJFq000UV-ZGssiOZSNG2ZWV7k53DCNdQJV4rmASzld6KC_o7giEppwnUT_CMWJIS7EFoNik01cEu5xOCDgE4Om19bLyhFu6sBL4545rpQLIrcGpAI1Ka8SOfcXYjIDiK4M82tz8Gi2F62ZrEjkl-TBoi8Hl9EKrdJaWuL7UFm_yZPsp9q0gSzw align="left")

When using the number notation, the 4 is the first value for the owner user, the 3 is the second value for the user group, and the 1 is the third value for the other group. The value is not only the permission access but also the entity.

### Not everyone needs all file permissions.

Not every user or group should have all file permissions. Grant permissions only when necessary, or it could jeopardize the security of your file.