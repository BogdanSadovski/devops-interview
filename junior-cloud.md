# DevOps Junior — Clouds

## 1. В чём разница между IaaS, PaaS и SaaS?

### IaaS (Infrastructure as a Service)

Провайдер предоставляет базовую инфраструктуру:

* виртуальные машины
* сети
* диски

**Примеры:** AWS EC2, GCP Compute Engine, Azure VM

Ответственность клиента:

* ОС
* приложения
* безопасность на уровне ОС

---

### PaaS (Platform as a Service)

Провайдер управляет платформой для запуска приложений.

**Примеры:** Heroku, Google App Engine

Клиент управляет:

* кодом приложения
* конфигурацией

---

### SaaS (Software as a Service)

Готовое приложение, доступное через интернет.

**Примеры:** Gmail, GitHub, Jira

Клиент только использует сервис.

---

## 2. Что такое VPC?

**VPC (Virtual Private Cloud)** — изолированная виртуальная сеть в облаке.

### Обычно включает:

* CIDR-блок
* subnets (public / private)
* route tables
* internet gateway / NAT gateway
* security groups / firewall rules

---

## 3. Зачем нужны public и private subnet?

* **Public subnet** — имеет доступ в интернет
* **Private subnet** — доступен только изнутри VPC

Типичный пример:

* Load Balancer — public
* Application / DB — private

---

## 4. Что такое Security Group?

Security Group — виртуальный firewall на уровне instance.

Особенности:

* stateful
* правила allow-only
* применяется к VM / LB

---

## 5. Что такое cloud-init?

`cloud-init` — механизм начальной инициализации VM.

Используется для:

* установки пакетов
* создания пользователей
* запуска скриптов при первом старте

### Пример:

```yaml
#cloud-config
packages:
  - nginx
runcmd:
  - systemctl start nginx
```

---

## 6. init, systemd, upstart — в чём разница?

* **init (SysV)** — старый, последовательный запуск
* **upstart** — событийный (устарел)
* **systemd** — современный стандарт

### Почему systemd лучше:

* параллельный запуск
* dependency management
* единый интерфейс

---

## 7. Что такое region и availability zone?

* **Region** — географический регион (eu-west-1)
* **AZ** — изолированный дата-центр внутри региона

Используется для отказоустойчивости.

---

## 8. Что такое elastic IP / static IP?

IP-адрес, который:

* не меняется
* можно привязывать к разным VM

Используется для:

* внешнего доступа
* failover

---

## 9. Что такое Load Balancer в облаке?

Load Balancer распределяет трафик между backend-сервисами.

### Типы:

* L4 (TCP)
* L7 (HTTP/HTTPS)

---

## 10. Что такое auto-scaling?

Auto-scaling — автоматическое изменение количества ресурсов.

Может быть:

* scale out / in
* scale up / down

Триггеры:

* CPU
* memory
* custom metrics

---

## 11. Основные преимущества облака

* быстрое масштабирование
* оплата по факту использования
* высокая доступность
* автоматизация

---

## 12. Основные недостатки облака

* vendor lock-in
* стоимость при неправильной настройке
* зависимость от провайдера

---

## 13. Shared Responsibility Model

Провайдер отвечает за:

* физическую инфраструктуру

Клиент отвечает за:

* данные
* конфигурацию
* доступы

---

## 14. Чем облако отличается от on-prem?

| Cloud         | On-prem    |
| ------------- | ---------- |
| Быстро        | Медленно   |
| OPEX          | CAPEX      |
| Масштабируемо | Ограничено |

---

## 15. Что важно сказать на собеседовании?

* понимать shared responsibility
* уметь объяснить VPC
* различать IaaS / PaaS / SaaS

---

✅ **Раздел Junior — Clouds завершён**
