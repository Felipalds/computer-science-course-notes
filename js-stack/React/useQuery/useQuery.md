
## Refetch
```
	const { data, refetch } = useQuery(myKey, fetchData)

	<button onClick={() => refetch()}>Pull data again!</button>
```