.PHONY: build up stop down ps exec

NM := app
CMD := bash

build:
	docker compose build

up:
	docker compose up -d

stop:
	docker compose stop

down:
	docker compose down;

ps:
	docker ps

exec:
	docker exec -it $(NM) $(CMD)
