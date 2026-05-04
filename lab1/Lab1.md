# 2025-cloud-platforms-U4125-truhin_m_s
# Cloud Platforms (2025–2026)

## ITMO University  
Faculty: FTMI  
Course: Cloud Platforms  
Group: U4125  
Student: Trukhin Maksim  


About the repository

The course covers:
- Google Cloud Platform (GCP)
- Cloud infrastructure basics
- Virtual machines and storage
- Access management (IAM)
- Practical cloud service usage


Repository structure
├── lab1/
│ ├── Lab1.md
│ └── images/
├── README.md
├── LICENSE
└── .gitignore


Lab 1 — Google Cloud Overview

Тема:  
Overview of Google Cloud and basic services

Что сделал:
- Created Service Account with IAM roles
- Created Virtual Machine (Compute Engine)
- Worked with Cloud Storage (gsutil)
- Copied files from bucket to VM
- Analyzed access rights and IAM behavior

## Ход работы

Шаг 1. Получение доступа к Google Cloud

Шаг 2. Создание Service Account

В разделе **IAM & Admin → Service Accounts** был создан сервисный аккаунт:

- Name: mtrukhin-sa-lab1

Сервисному аккаунту была назначена роль:

- Storage Admin

Это дало полный доступ к Cloud Storage.


Шаг 3. Создание виртуальной машины

В разделе Compute Engine → VM instances была создана виртуальная машина со следующими параметрами:

- Name: mtrukhin-vm-lab1
- Machine type: e2-micro
- Provisioning model: Spot


Шаг 4. Подключение к виртуальной машине

Подключение к VM было выполнено через SSH-интерфейс Google Cloud.


Шаг 5. Работа с Cloud Storage

Просмотр содержимого bucket

Была выполнена команда:

```bash
gsutil ls gs://lab1-bucket-itmo
Была создана локальная директория
Файлы были скопированы


Шаг 6. Проверка используемого 

По команде: gcloud auth list
Результат показал, что VM использует default Compute Engine service account: 307056602443-compute@developer.gserviceaccount.com

Шаг 7. Изменение ролей доступа
Storage Admin → Compute Viewer

Шаг 8. Очистка ресурсов

После завершения работы:

Виртуальная машина была удалена
Service Account может быть удалён при необходимости

Technologies used

- Google Cloud Platform (GCP)
- Compute Engine
- Cloud Storage
- IAM (Identity and Access Management)
- gcloud CLI
- gsutil


Автор

Trukhin Maksim 
ITMO University  
