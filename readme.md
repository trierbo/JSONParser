### JOSNParser
---
#### 1. Introduction
It's a json parser, for now, it can parse JSON string to JSON data format that defined in code, and it can format JSON data and print it.
#### 2. JSON Data Format
``` cpp
 typedef struct JSON {
    struct JSON *next, *prev;
    struct JSON *child;

    int type;
  
    char *valuestring; // type == JSON_String
    int valueint; // type == JSON_Number
    double valuedouble; // type == JSON_Number

    char *string; // name
  } JSON;
```
#### 3. JSON Parse
``` cpp
static const char *parse_string(JSON *item, const char *str);
static const char *parse_number(JSON *item, const char *num);
static const char *parse_value(JSON *item, const char *value);
static const char *parse_array(JSON *item, const char *value);
static const char *parse_object(JSON *item, const char *value);
```
- parse_string

![string](http://oanl5xf7d.bkt.clouddn.com//jsonparser/string.gif)

- parse_number

![number](http://oanl5xf7d.bkt.clouddn.com//jsonparser/number.gif)

- parse_value

![value](http://oanl5xf7d.bkt.clouddn.com//jsonparser/value.gif)

- parse_array

![array](http://oanl5xf7d.bkt.clouddn.com//jsonparser/array.gif)

- parse_object

![object](http://oanl5xf7d.bkt.clouddn.com//jsonparser/object.gif)
