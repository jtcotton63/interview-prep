# Java Streams API

### forEach

Note: both streams and collections have a forEach method. Be careful to distinguish the two.

```
empList.stream().forEach(e -> e.salaryIncrement(10.0));
```

### map

Produces a new stream after applying a function to each element of the original stream. The new stream could be of a different type.

```
Integer[] empIds = { 1, 2, 3 };
    
List<Employee> employees = Stream.of(empIds)
    .map(employeeRepository::findById)
    .collect(Collectors.toList());
```

### collect

Get stuff out of the stream once we are done processing

### filter

Produces a new stream that contains elements of the original stream that pass a given test

```

Integer[] empIds = { 1, 2, 3, 4 };
    
List<Employee> employees = Stream.of(empIds)
    .map(employeeRepository::findById)  # Isn't this a bad idea? Isn't it better to do this in bulk instead of a repo call for each item in the stream?
    .filter(e -> e != null)
    .filter(e -> e.getSalary() > 200000)
    .collect(Collectors.toList());
```

### findFirst

Returns an Optional for the first entry in the stream

### toArray

Collect method that creates an array

### flatMap

Continue: https://stackify.com/streams-guide-java-8/
Continue: https://www.youtube.com/watch?v=VRpHdSFWGPs