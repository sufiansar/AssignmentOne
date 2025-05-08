# Assignment

<!-- What are some differences between interfaces and types in TypeScript? -->

Interface and type Both are used to define the structure of object.
but there are many difference between them

##### Interface:

An interface kind of blueprint that tells what properties object will have,and what there type will be.

##### Type:

Its similer to Interface but its more fexible and it can be used to define union, intersection, tuples, function types etc.

now some are differecne between they.

Differences in syntax and usage

```
interface Person {
name: string;
age: number;
}

type person ={
interface Person {
name: string;
age: number;
}
```

##### extending: An interface extending multiple interfeces

##### type: similer to interface but its acces multiple types using (&)this symble.

##### decleration

Interface multiple interfaces with the same name can be combind together
type: When type uses multiple types with the same name its can be Error . because type can't accecss same name of type.

##### here example

```
interface User {
name: string;
}

interface User {
age: number;
}
```

here two interface declear with the same name but there is no Erro bcz interface combind together
and give the new interfaces

# <!-- What is the use of the keyof keyword in TypeScript? Provide an example. -->

##### keyof

keyof is a type operator that creates a union type of all the property names of an object or interface.
keyof helps find out which property names are in a type.
This is especially useful for writing safe code, as it can cause compile-time errors when we provide the wrong property name.

Here is an example of this:

```
type Person = {
name: string;
age: number;
};
```

Here we define the Person type.
type PersonKeys = keyof Person;
When we use the PersonKeys type and declare keyof Person,
then we see that the PersonKeys value will be "name" | "age".
That means PersonKeys is a type that can only be "name" or "age".
