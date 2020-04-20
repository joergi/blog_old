---
title: "Using MongoRepository with more than one sorting with Spring"
date: 2019-09-09
---

Sometimes you need a List of the Database to be sorted by more than one column.

If you connect to your database with the org.springframework.data.mongodb.repository.MongoRepository you can only give one org.springframework.data.domain.Sort to a search method.

This is how the Repository class looks like:
```Java
@Repository
public interface TestRepository extends MongoRepository<Test, Long> {
  public List<Score> findAllByTestName(String testName, Sort sort );
}
```
test has some column "abc" and some column "def" and some "ghi" ....
so to add the order do in th calling class something like:
```Java
Order abcOrder= new Sort.Order(Direction.DESC, "abc");
Order defOrder= new Sort.Order(Direction.ASC, "def");
Order ghiOrder= new Sort.Order(Direction.ASC, "ghi");       
```
So you use than the `org.springframework.data.domain.Sort.Order`
```Java
 testRepository.findAllByTestName(testName,new Sort(abcOrder, defOrder, ghiOrder));
```
You can now as as many as you need.
