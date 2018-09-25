# Reactive Adding Value to Existing Applications
## Spring Webflux


- Moores Law is No More
- New Functional features in Java 8 
- Now Let's go Async

## Client Side

WebClient
Functional, reactive, asynchronous, non-blocking, streaming
JAVA DSL

RestTemplate will be deprecated

## Server Side

in pom.xml
WEBFLUX
WEB

private webClient WebClient;

	@GetMapping("/person/{id}")
	Mono<Person> getPerson(@PathVariable Long id) {
		return this.client.get().uri("/person/{id}?delay=2", id)
				.retrieve()
				.bodyToMono(Person.class);
	}

	@GetMapping("/persons")
	Flux<Person> getPersons() {
		return client.get().uri("/persons?delay=2")
				.retrieve()
				.bodyToFlux(Person.class);
	}

    Servlets and Reactive Stacks

- Reactive Relational Database Connectivity
- Flight of the Flux
- Under the Hood of Reactive Data Access
