Сделано:
	•	Добавлен сценарий Molecule podman_lite для тестирования роли в контейнерах ubuntu:22.04 и rockylinux:8.
	•	Настроен tox (env py3) для запуска molecule test -s podman_lite --destroy always.
	•	Добавлен prepare.yml, который ставит python3 внутри контейнеров через raw (через /bin/sh -lc), затем собирает факты.
	•	Добавлены converge.yml (применение роли) и verify.yml (проверка наличия /usr/local/bin/vector).
	•	Molecule test проходит полностью: create → prepare → converge → idempotence → verify → destroy.


