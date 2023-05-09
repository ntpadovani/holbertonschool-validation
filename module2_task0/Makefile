# Variables
BINARY_NAME := awesome-api
LOG_FILE := $(BINARY_NAME).log
PID_FILE := $(BINARY_NAME).pid

# Goals
.PHONY: help

help: ## Prints out the list of targets and their usage
	@awk 'BEGIN {FS = ":.*?# "} /^[a-zA-Z_-]+:.*?# / {printf "\033[36m%-10s\033[0m %s\n", $$1, $$2}' $(MAKEFILE_LIST)


.PHONY: build
build: ## alsdjflksajdf a;ljsdflsadhf hf hdsa;lahdsf sdf;lkahds fhdsaf
	go get github.com/gorilla/mux
	go build -o $(BINARY_NAME)

.PHONY: run 
run: ## dslfjsaldjflkdsajfsajf;ljsadjf;lsajdfkldsaf sadfasdfasdfdsa
	./$(BINARY_NAME) > $(LOG_FILE) 2>&1 & echo $$! > $(PID_FILE)

.PHONY: stop
stop: ## dsakjhfalsd hf;lsa fjdsahf;sahfhsadlkfhsadfsafd 
	-kill `cat $(PID_FILE)` || true
	-rm $(PID_FILE) || true


.PHONY: clean 
clean: ## sa;lkdjf dsasadlkjfsad f;lj hdsaflja'skjd flkas
	make stop
	-rm $(BINARY_NAME) || true
	-rm $(LOG_FILE) || true

.PHONY: test
test: ## WOOOHOOOOOOOO saljdfasldhfaksdf asdsafgasgasfasdf
	@echo "Testing HTTP endpoint /..."
	@curl -sSf http://localhost:9999 || echo "TESTFAILED"
	@echo "Testing HTTP endpoint /health..."
	@curl -sSf http://localhost:9999/health || echo "TESTFAILED"

.PHONY: lint
lint: ## LINT LINT LINT YEAHHHH BABYYYY
	golangci-lint run

