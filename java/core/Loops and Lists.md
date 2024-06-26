
## Lists (Collections)
- List is an ordered collection of elements
- Allow duplicate elements
- Provide indexed access to elements
- Mutable

## Streams
- Sequence of elements which can be easily obtained from a Collection.
- Sequence of elements that can be processed sequentially or in parallel
- Supports filter, map, reduce, forEach
- Supports lazy evaluation
- A stream is not a data structure! It takes input from collections
- Doesnt change the original data structure
- Returns a stream in every pipeline
- Does not store data! Operates instead.
- Lambda functions
- Not modifiable
```
	List<String> companyList = new ArrayList<>();

	// Adding elements to above ArrayList
	companyList.add("Google");
	companyList.add("Apple");
	companyList.add("Microsoft");

	// Sorting the list
	// using sorted() method and
	// printing using for-each loop
	companyList.stream().sorted().forEach(System.out::println);
```
https://www.geeksforgeeks.org/difference-between-streams-and-collections-in-java/
https://mmarcosab.medium.com/usando-streams-no-java-b85d98d9cf17

## Maps
Mapping keys to values

## ForEach
```
	data.getProducts().forEach(product -> product.setDiscount(10))
```