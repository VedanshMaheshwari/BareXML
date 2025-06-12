# BareXML
"The bare essentials of XML parsing in C — no bloat, just results." --inplemented from scratch.

LMX is a simple yet functional XML parser written in C. It parses basic XML structure including nested tags, attributes, and text content, and displays the parsed data in a clean, human-readable format.

This project is great for understanding how XML parsers work under the hood, especially for educational purposes or systems-level parsing where external libraries aren't ideal.

---

## 🔧 Features

- Parses XML tags with attributes
- Handles nested and hierarchical elements
- Supports multiple root-level tags
- Reads and prints text content from tags
- Detects and reports mismatched or missing closing tags
- Gracefully skips whitespace and formats clean output

---

## 🛠️ Build Instructions

1. Clone or download the project.
2. Ensure you have GCC or another C compiler installed.
3. Compile the project:

```bash
gcc main.c lmx.c -o lmx

Sample Input
```<catalog>
  <book id="1" genre="fiction">
    <title>The Great Gatsby</title>
    <author>F. Scott Fitzgerald</author>
  </book>
  <book id="2" genre="sci-fi">
    <title>Dune</title>
    <author>Frank Herbert</author>
  </book>
</catalog>

<university>
  <student id="S1">
    <name>John Doe</name>
    <age>21</age>
    <courses>
      <course code="CS101">Computer Science</course>
      <course code="MA201">Mathematics</course>
    </courses>
  </student>
</university>

Sample Output
Tag: <catalog>
Tag: <book>
  Attribute - id: 1
  Attribute - genre: fiction
Tag: <title>
  Text: The Great Gatsby
Tag: <author>
  Text: F. Scott Fitzgerald

Tag: <book>
  Attribute - id: 2
  Attribute - genre: sci-fi
Tag: <title>
  Text: Dune
Tag: <author>
  Text: Frank Herbert

Tag: <university>
Tag: <student>
  Attribute - id: S1
Tag: <name>
  Text: John Doe
Tag: <age>
  Text: 21
Tag: <courses>
Tag: <course>
  Attribute - code: CS101
  Text: Computer Science
Tag: <course>
  Attribute - code: MA201

  Text: Mathematics
