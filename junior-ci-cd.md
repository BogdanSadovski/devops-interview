# DevOps Junior — CI/CD

## 1. Что такое CI/CD?

**CI/CD (Continuous Integration / Continuous Delivery)** — практика автоматизации сборки, тестирования и доставки приложения.

* **CI** — частая интеграция кода в общий репозиторий
* **CD** — автоматическая доставка или деплой

---

## 2. Зачем нужен CI/CD?

CI/CD позволяет:

* быстрее находить ошибки
* уменьшить ручной труд
* ускорить выпуск релизов
* повысить стабильность

---

## 3. Что такое pipeline?

Pipeline — это последовательность шагов, которые выполняются автоматически.

Обычно включает:

* build
* test
* deploy

---

## 4. Из каких этапов состоит CI pipeline?

Типичный CI pipeline:

1. Checkout кода
2. Build
3. Unit tests
4. Lint / static analysis
5. Artifacts

---

## 5. Что такое CD?

CD может быть:

* **Continuous Delivery** — деплой по кнопке
* **Continuous Deployment** — деплой автоматически

На Junior уровне важно знать разницу.

---

## 6. Что такое artifact?

Artifact — результат сборки pipeline.

Примеры:

* бинарник
* Docker image
* архив

---

## 7. Что такое runner / agent?

Runner — машина, которая выполняет pipeline.

Может быть:

* shared
* self-hosted

---

## 8. GitLab CI vs GitHub Actions

| GitLab CI      | GitHub Actions      |
| -------------- | ------------------- |
| .gitlab-ci.yml | workflows/*.yml     |
| Встроенный CI  | Интеграция с GitHub |

---

## 9. Пример GitLab CI pipeline

```yaml
stages:
  - build
  - test

build:
  stage: build
  script:
    - echo "Build"

test:
  stage: test
  script:
    - echo "Test"
```

---

## 10. Пример GitHub Actions workflow

```yaml
name: CI
on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - run: echo "Build"
```

---

## 11. Что такое environment?

Environment — окружение для деплоя:

* dev
* stage
* prod

Каждое окружение может иметь свои настройки.

---

## 12. Что такое secrets?

Secrets — чувствительные данные:

* пароли
* токены
* ключи

Хранятся в CI-системе, а не в коде.

---

## 13. Что такое rollback?

Rollback — откат к предыдущей версии приложения.

Важно для:

* аварий
* неудачных релизов

---

## 14. Best practices CI/CD для Junior

* pipeline должен быть быстрым
* секреты не хранить в репозитории
* автоматизировать тесты

---

## 15. Что важно сказать на собеседовании?

* CI/CD автоматизирует путь от кода до продакшена
* artifact — результат сборки
* pipeline состоит из stages и jobs

---

✅ **Раздел Junior — CI/CD завершён**
