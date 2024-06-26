# Cascade:
https://www.baeldung.com/jpa-cascade-types
We have relations between our classes. For example, person and address. Every address should have a person, in other case, it does not have sense for existing. When we delete a person, the address must be deleted too.

javax.persistence.CascadeType enum:
- ALL
- PERSIST
- MERGE
- REMOVE
- REFRESH
- DETACH

org.hibernate.annotations.CascadeType:
- REPLICATE
- SAVE_UPDATE
- LOCK

## ALL:
Propagates all operations - including Hibernate - from a parent to a child entity.
```
@Entity
public class Person {
	@Id
	@GeneratedValue(strategy = GenerationType.AUTO)
	private int id;

	private String name;

	@OneToMany(mappedBy = "person", cascade = CascadeType.ALL)
	private List<Address> addresses;
}


@Entity
pubic class Address {
	@Id
	@GeneratedValue(strategy = GenerationType.AUTO)
	private int id;

	@ManyToOne(fetch = FetchType.LAZY)
	private Person person.

}

```

## PERSIST
When we save a person, the address will also get saved.

## MERGE
The merge operations copies the state of the given object onto the persistent object with the same identifier. Propagates the merge operation from a parent to a child entity.