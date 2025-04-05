
# XML vs JSON: Key Differences

## 📌 Basic Definitions

**XML (eXtensible Markup Language):**
```xml
<person>
  <name>John Doe</name>
  <age>30</age>
  <city>New York</city>
</person>
```

**JSON (JavaScript Object Notation):**
```json
{
  "person": {
    "name": "John Doe",
    "age": 30,
    "city": "New York"
  }
}
```

---

## 🔍 Key Differences

| Feature              | XML                           | JSON                             |
|----------------------|-------------------------------|----------------------------------|
| Format Type          | Markup language               | Data interchange format          |
| Syntax               | Tag-based (`<tag>`)           | Key-value pairs                  |
| Readability          | Verbose                       | More concise                     |
| Parsing              | Requires XML parser           | Native JavaScript support        |
| Data Types           | Everything is text            | Supports numbers, booleans, etc. |
| Metadata Support     | Yes (attributes, namespaces)  | No                               |
| Array Representation | Implicit                      | Explicit                         |
| Comments             | Supported                     | Not supported                    |

---

## ⚡ Performance Comparison

- **Size:** JSON is typically 30–40% smaller  
- **Parsing Speed:** JSON parses 2–10x faster  
- **Memory Usage:** JSON requires less memory  

---

## 🌐 Usage Scenarios

**When to use XML:**
- Document markup (e.g., HTML, DOCX)
- Complex data with metadata
- Legacy systems / SOAP web services
- When human readability is important

**When to use JSON:**
- Web APIs (RESTful services)
- Configuration files
- Mobile apps
- Real-time data transfer
- When performance is critical

---

## 🔧 Conversion Example

**XML to JSON:**
```xml
<book>
  <title>JavaScript Guide</title>
  <price>29.99</price>
</book>
```

→ **Equivalent JSON:**
```json
{
  "book": {
    "title": "JavaScript Guide",
    "price": 29.99
  }
}
```

---

## ✅ Advantages

**XML Advantages:**
- Self-descriptive format
- Strong validation (XSD)
- Supports mixed content
- Better for document storage

**JSON Advantages:**
- Lightweight
- Native JavaScript support
- Easier to parse
- Better for APIs

---

## ⚠️ Limitations

**XML Limitations:**
- Verbose syntax
- Complex parsing
- No direct data typing

**JSON Limitations:**
- No comments
- No namespace support
- Limited tooling for validation
