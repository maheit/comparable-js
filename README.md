# comparable-js
A rich, modern and optimistic Javascript library to different datatype deep comparison, validation and model generation


**Install Package from npm register**
``` npm install -S comparable ```

**Import function for comparison which do deep equal on individual data not on shallow references**

``` import { isDeepEqual } from "comparable" ```

OR

``` 
import comparable from "comparable" 
comparable.isDeepEqual(a, b)

```

then compare any two value, here is one example:

```

const previousUserDetails = [
  {
    _id: "6485d7b3910143f6c6612e43",
    index: 0,
    guid: "0d12fcb9-60cb-44c8-9c0b-3291000e101f",
    isActive: false,
    balance: "$3,190.82",
    picture: "http://placehold.it/32x32",
    age: 36,
    eyeColor: "brown",
    name: "Carroll Whitfield",
    gender: "male",
    company: "UNI",
    email: "carrollwhitfield@uni.com",
    phone: "+1 (825) 495-2976",
    address: "624 Harden Street, Hebron, New York, 9263",
    about:
      "Dolore aliquip fugiat eiusmod deserunt officia do sit veniam qui ipsum mollit velit aliquip. Consequat pariatur labore duis eiusmod labore cillum. Minim dolor cillum id veniam nisi reprehenderit non proident sit ea. Voluptate eiusmod nostrud esse ipsum. Velit velit mollit ut sit esse irure. Enim magna eu aute amet adipisicing ad ut incididunt dolor minim mollit enim sunt irure. Qui velit excepteur eu nostrud ipsum id cupidatat cupidatat pariatur veniam proident duis.\r\n",
    registered: "2015-05-29T12:40:20 -06:-30",
    latitude: -83.967232,
    longitude: 166.790436,
    tags: ["sunt", "duis", "sit", "consectetur", "eiusmod", "culpa", "anim"],
    friends: [
      {
        id: 0,
        name: "Ashley Lyons",
      },
      {
        id: 1,
        name: "Ophelia Erickson",
      },
      {
        id: 2,
        name: "Britney Cook",
      },
    ],
    greeting: "Hello, Carroll Whitfield! You have 6 unread messages.",
    favoriteFruit: "apple",
  },
  {
    _id: "6485d7b37b1dc2e7fca2fcb8",
    index: 1,
    guid: "3abd33c4-ecc7-4f1b-947b-5da8fae10eb6",
    isActive: false,
    balance: "$2,934.49",
    picture: "http://placehold.it/32x32",
    age: 24,
    eyeColor: "brown",
    name: "Nunez Gilliam",
    gender: "male",
    company: "LIQUIDOC",
    email: "nunezgilliam@liquidoc.com",
    phone: "+1 (807) 482-3613",
    address: "753 Oriental Boulevard, Madrid, Hawaii, 1447",
    about:
      "Consectetur est pariatur sint laborum adipisicing id eu mollit quis. Do ex ullamco sint et ullamco consectetur aliqua deserunt aliquip ex adipisicing duis. Aliqua aute consectetur non occaecat cillum Lorem. Velit voluptate qui ad eiusmod incididunt. Id adipisicing occaecat nisi consectetur. Irure enim reprehenderit nulla aliquip eu enim laboris fugiat commodo Lorem sit.\r\n",
    registered: "2018-01-18T07:24:57 -06:-30",
    latitude: 13.025603,
    longitude: -105.261093,
    tags: ["non", "cillum", "quis", "incididunt", "veniam", "tempor", "ipsum"],
    friends: [
      {
        id: 0,
        name: "Katherine Wilkerson",
      },
      {
        id: 1,
        name: "Pruitt Robertson",
      },
      {
        id: 2,
        name: "Marsha Battle",
      },
    ],
    greeting: "Hello, Nunez Gilliam! You have 3 unread messages.",
    favoriteFruit: "banana",
  },
];

const newUserDetails = [
  {
    _id: "6485d7b3910143f6c6612e43",
    index: 0,
    guid: "0d12fcb9-60cb-44c8-9c0b-3291000e101f",
    isActive: false,
    balance: "$3,190.82",
    picture: "http://placehold.it/32x32",
    age: 36,
    eyeColor: "brown",
    name: "Carroll Whitfield",
    gender: "male",
    company: "UNI",
    email: "carrollwhitfield@uni.com",
    phone: "+1 (825) 495-2976",
    address: "624 Harden Street, Hebron, New York, 9263",
    about:
      "Dolore aliquip fugiat eiusmod deserunt officia do sit veniam qui ipsum mollit velit aliquip. Consequat pariatur labore duis eiusmod labore cillum. Minim dolor cillum id veniam nisi reprehenderit non proident sit ea. Voluptate eiusmod nostrud esse ipsum. Velit velit mollit ut sit esse irure. Enim magna eu aute amet adipisicing ad ut incididunt dolor minim mollit enim sunt irure. Qui velit excepteur eu nostrud ipsum id cupidatat cupidatat pariatur veniam proident duis.\r\n",
    registered: "2015-05-29T12:40:20 -06:-30",
    latitude: -83.967232,
    longitude: 166.790436,
    tags: ["sunt", "duis", "sit", "consectetur", "eiusmod", "culpa", "anim"],
    friends: [
      {
        id: 0,
        name: "Ashley Lyons",
      },
      {
        id: 1,
        name: "Ophelia Erickson",
      },
      {
        id: 2,
        name: "Britney Cook",
      },
    ],
    greeting: "Hello, Carroll Whitfield! You have 6 unread messages.",
    favoriteFruit: "apple",
  },
  {
    _id: "6485d7b37b1dc2e7fca2fcb8",
    index: 1,
    guid: "3abd33c4-ecc7-4f1b-947b-5da8fae10eb6",
    isActive: false,
    balance: "$2,934.49",
    picture: "http://placehold.it/32x32",
    age: 24,
    eyeColor: "brown",
    name: "Nunez Gilliam",
    gender: "male",
    company: "LIQUIDOC",
    email: "nunezgilliam@liquidoc.com",
    phone: "+1 (807) 482-3613",
    address: "753 Oriental Boulevard, Madrid, Hawaii, 1447",
    about:
      "Consectetur est pariatur sint laborum adipisicing id eu mollit quis. Do ex ullamco sint et ullamco consectetur aliqua deserunt aliquip ex adipisicing duis. Aliqua aute consectetur non occaecat cillum Lorem. Velit voluptate qui ad eiusmod incididunt. Id adipisicing occaecat nisi consectetur. Irure enim reprehenderit nulla aliquip eu enim laboris fugiat commodo Lorem sit.\r\n",
    registered: "2018-01-18T07:24:57 -06:-30",
    latitude: 13.025603,
    longitude: -105.261093,
    tags: ["non", "cillum", "quis", "incididunt", "veniam", "tempor", "ipsum"],
    friends: [
      {
        id: 0,
        name: "Katherine Wilkerson",
      },
      {
        id: 1,
        name: "Pruitt Robertson",
      },
      {
        id: 2,
        name: "Marsha Battle",
      },
    ],
    greeting: "Hello, Nunez Gilliam! You have 3 unread messages.",
    favoriteFruit: "banana",
  },
];

console.log(isDeepEqual(newUserDetails, previousUserDetails));

console.log("str", "int");
console.log("str", 10);
console.log({}, null);
console.log(undefined, [1] );


```

# Meta object optional third parameter for custom comparison for deep equal (with default value)

1. exactObject = true - this allows lazy equal when we set as false example one object may have more property than another object but it should include all the property of another object. other wise both are exactly should have same number property and value
2. exactArray = true - this allows lazy equal when we set as false example one array  may have more item than another another but it should include all the item of another array. other wise both are exactly should have same number items and value
3. swapCompObject = true (swapComparisonObject) - by default we are allowing to interchange passing arrgument to compare objects. example if you call isDeepEqual function with first argument as "A" and second argument as "B", while comparision this can be interchangeable for better comparison so it could inverted first argument as "B" then second as "A". while setting this as "false" we can restrict this inversion. 
4. swapCompArray = true (swapComparisonArray) - by default we are allowing to interchange passing arrgument to compare objects. example if you call isDeepEqual function with first argument as "A" and second argument as "B", while comparision this can be interchangeable for better comparison so it could inverted first argument as "B" then second as "A". while setting this as "false" we can restrict this inversion.

# Example with meta arguments:
```
console.log(isDeepEqual([1, 2, 3], [2, 1], { exactArray: false })); // true, because all the items in minimum length (second argument) array present in another array (first argument).

console.log(isDeepEqual([11, 3], [21, 1, 3, 11], { swapCompArray: false, exactArray: false })); // true, because all the items in first argument array present in second argument array.

console.log(isDeepEqual({ name: "Maheshwaran G" }, {} , { exactObject: false, swapCompObject: false })); // false, because second argument object atleast should include all the property of first argument object.

console.log(isDeepEqual({ name: "Maheshwaran G" }, {} , { exactObject: false })); // true, since swap of argument possible due to default swapComparisonObject as true so second argument has the minimum property than first then it means another object (first argument) has all the property of seconf argument object so it return true.

```

Please post your requirements that you want along with this feature we will put best effort to bring them to all the users.
If you found any bug Please raise Bug or write mail to maheitdev@gmail.com or create PR with fixes , we will validate and put best effort to bring them to all the users.

Thank you. 
