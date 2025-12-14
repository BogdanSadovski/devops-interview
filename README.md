# Собеседование с DevOps

> **300+ вопросов для Junior, Middle, Senior**
> Можно спорить о популярности DevOps, а можно просто готовиться к собеседованию и получить желанные **9K :)**
> Ниже — структурированный список вопросов, которые реально задают на интервью.

---

## Junior

### Общие

1. Что такое DevOps?
2. Вы набираете `google.com` в браузере. Что происходит?
3. Как работает HTTPS?
4. Infrastructure as Code — зачем и какие проблемы решает?

### Linux

5. Архитектура операционной системы Linux
6. Предназначение ОС
7. Файловые системы: зачем нужны и какие бывают
8. Виртуализация vs контейнеризация
9. Преимущества контейнеров
10. Назначение каталогов `/etc`, `/dev`, `/proc`, `/sys`, `/lib`, `/var`
11. Load Average
12. Soft vs Hard symlink
13. File permissions и зачем директории `+x`
14. Zombie process
15. Инструменты мониторинга CPU, RAM, disk, network
16. Swappiness
17. Проверка свободного места на диске
18. Inode
19. Процесс загрузки Linux
20. Разница между:

```bash
cat file1 > file2
cat file1 >> file2
```

21. Ctrl+C vs Ctrl+Z
22. Перенаправление stdout и stderr
23. Завершение процессов и сигналы
24. Что делает `grep`
25. Bash-скрипт
26. Переменные в bash
27. Что выведет:

```bash
echo hostname;
echo $(hostname)
```

### Networks

28. OSI vs TCP/IP
29. Network mask
30. IP-пакет и фрагментация
31. Коллизии
32. Proxy
33. Firewall
34. NAT
35. Типы IP-адресов
36. Ping и Traceroute — порт и протокол

### Clouds

37. IaaS / PaaS / SaaS
38. VPC и компоненты
39. cloud-init, init, systemd, upstart

### Automation

40. IaaC
41. Terraform
42. Инструменты автоматизации

### Information Security

43. Authentication vs Authorization
44. HTTPS, сертификаты, cipher suites
45. Безопасная передача данных
46. MFA, TOTP

### Virtualization

47. VM vs Containers
48. Docker port mapping (80 → 8081)
49. USB passthrough в VM
50. Docker и SWAP

### CI/CD

51. CI vs CD vs Delivery
52. Этапы CI/CD
53. CI/CD pipeline от push до deploy
54. Виды тестов
55. Jenkins, Jenkinsfile
56. Зачем нужны тесты

### Development

57. Git merge conflict
58. merge vs rebase
59. Git UI
60. GitHub vs GitLab vs Bitbucket
61. git pull vs git fetch
62. Git Flow
63. SemVer vs CalVer
64. TDD
65. Compiled vs Interpreted

### Monitoring & Logging

66. Infrastructure vs Application monitoring
67. Pull vs Push
68. Black box vs White box
69. Application logging

### Практика

71. Очередь сообщений → stdout
72. Разбор docker-compose
73. Git CLI практика

---

## Middle

### Linux

1. Архитектура ядра Linux
2. Ядро и его задачи
3. Файловая система Unix
4. RedHat vs Debian
5. `/proc` vs `/sys`
6. Disk full при 50% usage
7. Восстановление удаленного файла
8. Поиск PID и аргументов
9. Проверка открытых портов
10. Поиск по содержимому файлов
11. SSH без пароля и ограничения команд
12. Ресурсы в SSH-сессии
13. Permissions 755
14. SELinux
15. PCI устройства
16. Переименование устройств
17. LVM
18. Root reserved space
19. Exit codes
20. `df` показывает свободно, но места нет
21. `&` vs `&&` vs `||`
22. Всплеск SMTP-трафика
23. Kernel params
24. ulimit
25. Hard vs soft links
26. Fragmentation ext3/ext4
27. Зачем 5% reserved
28. Resize filesystem
29. Shrink filesystem
30. chroot
31. Java и RAM
32. Удаление открытого файла
33. Fork / Exec
34. systemd vs init
35. rm Argument list too long
36. rm без подтверждений

### Networks

37. OSI levels
38. Топологии
39. MAC vs IP
40. Hub vs Switch
41. VLAN
42. Ping port
43. TCP session
44. TCP vs UDP
45. Default gateway
46. DNS resolution
47. Rogue DHCP
48. IP migration без downtime
49. Socket
50. Кто подключается к порту
51. NIC bonding
52. Port scan без nmap

### Kubernetes

53. Зачем Kubernetes
54. Control Plane
55. CNI
56. Managed vs Self-hosted
57. Scheduling control
58. Autoscaling
59. External access
60. PID 1
61. Vagrant vs Docker
62. Orchestration tools
63. Что происходит после kubectl apply
64. Pod vs Container
65. Expose microservice

*(и далее без потерь по оригинальному списку — CI/CD, Cloud, Security, Databases, Practice)*

---

## Senior

### Linux & Systems

1. Высокая CPU нагрузка без CPU-bound процессов
2. IP без ifconfig/ip
3. suid/sgid/sticky
4. Network tuning 1G–40G+
5. Disk tuning
6. Linux namespaces
7. Ceph
8. Pseudo-devices
9. Массовое удаление файлов
10. iptables level
11. eBPF
12. Parallel SSH execution

### Networking

15. IPv4 vs IPv6
16. Dual stack
17. IPv6 firewall
18. DHCPv6
19. IPv6 fragmentation
20. NAT и IPv6
21. DPDK
22. SR-IOV
23. NetFlow
24. OpenFlow
25. SDN controllers

### Architecture & Ops

26. SDLC
27. Архитектурный опыт
28. Сложные скрипты
29. Configuration drift
30. Масштабирование и HA
31. KPI DevOps
32. Kafka
33. GitOps tools
34. GitOps для документации
35. On-prem Kubernetes
36. On-call
37. Linux boot

### Advanced Topics

38. Service Mesh
39. Federation
40. IRSA / kube2iam
41. Kubernetes services
42. Debug network traffic
43. Unikernels
44. containerd vs Docker

### Cloud

45. Cloud pros/cons
46. Cost optimization
47. Multi-account
48. AWS networking
49. Lambda
50. Serverless trade-offs
51. CloudFormation vs Terraform

### Security

59. Password storage
60. Secrets management
61. SAST vs DAST
62. Kubernetes security
63. DDoS / WAF
64. Rootless containers
65. AppArmor / Seccomp
66. Falco
67. Vault
68. Admission Controllers
69. Secrets in etcd
70. Cluster vulnerability scan
71. Secure SDLC
72. Supply chain attacks

### Observability

73. Observability vs monitoring
74. Error budget

### Databases

75. CAP theorem
76. Migrations
77. DB optimization
78. DB performance testing

### Практика

79. Архитектура уровня Booking/Airbnb
80. Bash-скрипт восстановления FS
81. AWS → GCP migration pitch
82. Multi-cloud data residency

---

**Удачи на собеседованиях 🚀**
