# 1. Avoid repetitive code
- Lombok is a tool to make us more productive
- Auto generates Java bytecode into our .class files as annotations we introduce in our code

# 2. Getters and Setters
- Generates @Getters and @Setters
- Generates @NoArgsConstructor
- @Setter (AccessLevel.PROTECTED) to a field

# 3. Lazy Getter
- Performance
- Gets something only if it is NULL. 

```
public class GetLazy {

	@Getter(lazy = true)
	private final Map<String, Long> transactions = getTransactions();

	private Map<String, Long> getTransactions() { final Map<String, Long> cache = new HashMap<>(); List<String> txnRows = readTxnListFromFile(); txnRows.forEach(s -> { String[] txnIdValueTuple = s.split(DELIMETER); cache.put(txnIdValueTuple[0], Long.parseLong(txnIdValueTuple[1])); }); return cache; }

}

```

- If the variable is NULL, then execute the function and cache it as a simple getter.


# DTOs
- @RequiredArgsConsctuctor annotation sets a constructor for all the final fields in the class
- @NonNull checks for nullability
- @Accessors(fluent=true) change the getters from getVar to simply var()


# Builder
```

User.builder().a().b().build()
```

# @Syncronyze (ThreadSafe)