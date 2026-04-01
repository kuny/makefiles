
.PHONY: all build dev

DEBUG_URL = "http://localhost:8080"

all: build

build:
	npm run build

dev:
	@if [ "$$(uname)" = "Darwin" ]; then \
		open $(DEBUG_URL); \
	elif [ "$$(uname)" = "Linux" ]; then \
		xdg-open $(DEBUG_URL); \
	elif [ "$$OS" = "Windows_NT" ]; then \
		start $(DEBUG_URL); \
	else \
		echo "対応していないOSです"; \
	fi
	npm run dev -- --port=8080
