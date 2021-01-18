To start server:

```
./gradlew -p config-server bootRun&
```

You can tets it with:

```
curl localhost:8888/config-client/default
```

To start client:

```
./gradlew -p config-client bootRun
```

The expected result is "demo property value: Bob" being printed to stdout.
The observer result is an exception being thrown.

The client uses Spring Boot 2.4.2. Downgrading it to 2.4.1  fixes the problem.
