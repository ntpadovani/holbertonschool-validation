# Variables
BINARY_NAME := awesome-api
LOG_FILE := $(BINARY_NAME).log
PID_FILE := $(BINARY_NAME).pid

# Goals
.PHONY: help

help: ## Prints out the list of targets and their usage
	@awk 'BEGIN {FS = ":.*?# "} /^[a-zA-Z_-]+:.*?# / {printf "\033[36m%-10s\033[0m %s\n", $$1, $$2}' $(MAKEFILE_LIST)


.PHONY: build
build: lint ## alsdjflksajdf a;ljsdflsadhf hf hdsa;lahdsf sdf;lkahds fhdsaf
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
	-make stop
	-rm -f ./awesome-api ./awesome-api.log coverage*

.PHONY: test
test: unit-tests integration-tests ## WOOOHOOOOOOOO saljdfasldhfaksdf asdsafgasgasfasdf



.PHONY: lint
lint: ## LINT LINT LINT YEAHHHH BABYYYY
	golangci-lint run

.PHONY: unit-tests
unit-tests: ## UNIT TEST UNIT TEST
	go test -v -short -coverprofile=coverage-units.out

.PHONY: integration-tests 
integration-tests: ## " - integration-tests: Runs the Golang integration tests"
	go test -v -coverprofile=coverage-integrations.out

