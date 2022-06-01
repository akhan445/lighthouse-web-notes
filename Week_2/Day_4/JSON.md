# JSON

**JSON** stands for JavaScript Object Notation
- subset of js language so all syntax **matches valid js**

JSON is built with two structures:
- a collection of name/value pairs
- an ordered list of values
- JSON is language independant

*Object* encoded using JSON:

```javascript
{
  "name": "New York City",
  "boroughs": [
    "Manhattan",
    "Queens",
    "Brooklyn",
    "The Bronx",
    "Staten Island"],
  "population": 8491079,
  "area_codes": [212, 347, 646, 718, 917, 929],
  "position": { "lat": 40.7127, "lng": -74.0059 }
}
```
`keys`   --> always strings

`values` --> can be anything

## **Serialization**

Serialization involves in converting objects/data structures into a format that can be stored/transmitted between computers
- usually to string/text

Serialization   = `Object` --> `String`

Deserialization = `String` --> `Object`

in JS, the **JSON object** can be used for serializing and deserializing

```javascript
JSON.parse() // Parse a string as JSON

JSON.stringify() // Return a JSON string corresponding to the specified value
```