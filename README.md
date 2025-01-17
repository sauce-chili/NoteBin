## Purpose

This project was created as a training project within the framework of the university discipline of "Information Systems Design".

## Fuatures

The project is largely inspired by PasteBin. The following features were implemented during development:

* __Several storage modes__ - in PasteBin you can create a note with 3 storage modes (“Burn after read”, “Burn by period”, “Never”).
  The most interesting is the first one. It allows you to read the note only once (even with simultaneous requests, the note will be issued only to one).
  NoteBin supports it. This feature is implemented through Redis transactions and optimistic locking;
  
* __Notes Caching__ - сache the most frequently requested data using Redis;

* __Unique short URL__ - we give the user short and unique URL. The URL is provided instantly, our user does not wait for it to be generated.
For this, 2 types of pools of free (pre-generated) URLs are used: local and global. Pools are replenished in asynchronous mode when “starvation” is detected;

* __Acount system__ - system allows registered accounts through which you can view and edit previously created notes.
  User authentication is performed on the basis of a JWT with 2 types of tokens: refresh and access;

* __Analytics__ - collecting information on views of notes. Statistics on the number of non/unique views are available.

## Stack Overview

<p align="center">
  <img src="https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=black" alt="Java">
  <img src="https://img.shields.io/badge/kotlin-%237F52FF.svg?style=for-the-badge&logo=kotlin&logoColor=white" alt="Kotlin">
  <img src="https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white" alt="Spring">
  <img src="https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white" alt="Postgres">
  <img src="https://img.shields.io/badge/Hibernate-59666C?style=for-the-badge&logo=Hibernate&logoColor=white" alt="Hibernate">
  <img src="https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white" alt="Redis">
  <img src="https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20web%20tokens" alt="JWT">
  <img src="https://img.shields.io/badge/Gradle-02303A.svg?style=for-the-badge&logo=Gradle&logoColor=white" alt="Gradle">
  <img src="https://img.shields.io/badge/apache%20tomcat-%23F8DC75.svg?style=for-the-badge&logo=apache-tomcat&logoColor=black" alt="Apache Tomcat">
  <img src="https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
</p>

