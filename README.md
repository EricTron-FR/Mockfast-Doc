# MockFast.io - Mock as a Service

[![Website](https://img.shields.io/badge/Visit-MockFast.io-blue)](https://mockfast.io)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

<p align="center">
  <img src="./mockfast-og.png" alt="MockFast Logo" width="200"/>
</p>

## 🚀 What is MockFast?

MockFast is a "Mock as a Service" platform that lets developers create and deploy custom mock APIs in seconds without writing any backend code. Perfect for frontend development, testing, and API prototyping.

**With MockFast, you can:**
- Create realistic API endpoints by simply defining your data structure
- Access a rich library of data types from basic to specialized (names, addresses, analytics, etc.)
- Deploy instantly to a reliable, production-ready environment
- Generate complex, nested data structures with array multipliers

## 📚 Documentation

This repository contains the official documentation for MockFast.io. Use the links below to navigate to relevant sections:

- [Quick Start Guide](./docs/quick-start.md)
- [Using MockFast](./docs/using-mockfast.md)
- [Data Types Reference](./docs/data-types.md)
- [Complex Templates](./docs/complex-templates.md)

## 🔍 Quick Start

### 1. Define Your Template

```json
{
  "name": "string",
  "age": "number",
  "email": "email"
}
```

### 2. Get Your API Endpoint

```
https://mockfast.io/api/YOUR_ID
```

### 3. Use Your API

```javascript
fetch('https://mockfast.io/api/YOUR_ID')
  .then(response => response.json())
  .then(data => console.log(data));
```

## 📋 Available Data Types

MockFast supports a wide range of data types:

### Basic Types
- `string` - Random text strings
- `number` - Random numbers
- `boolean` - True/false values
- `email` - Valid email addresses
- `uuid` - Unique identifiers
- `date` - Date strings
- `lorem` - Lorem ipsum text

### Advanced Types
- **Name types** - Generate realistic names (fullname, firstname, lastname)
- **Address types** - Generate address components or full addresses
- **Mail types** - Email addresses from various providers
- **Money types** - Currencies, symbols, and prices
- **Review types** - Rating numbers and review text
- **Country types** - Country information and metadata
- **Event types** - Event details including venues and dates
- **Color types** - Color codes in various formats
- **File types** - File metadata and path information
- **Weather types** - Weather conditions and location data
- **Analytics types** - Website analytics and metrics

## 💡 Advanced Features

### Array Multipliers

Generate multiple items dynamically with the special `__multiply` property:

```json
{
  "categories": [
    {
      "__multiply": "2-5",
      "name": "string",
      "id": "uuid"
    }
  ]
}
```

This generates between 2-5 category objects, each with random data.

### Complex Nested Structures

Create realistic API responses with nested objects and arrays:

```json
{
  "user": {
    "name": "string.name.fullname",
    "email": "email",
    "orders": [
      {
        "__multiply": "3-8",
        "orderId": "uuid",
        "total": "number.money.price",
        "items": [
          {
            "__multiply": "1-4",
            "productId": "uuid",
            "name": "string",
            "price": "number.money.price"
          }
        ]
      }
    ]
  }
}
```

## 💼 Plans and Features

### Free Plan
- Create basic mock APIs with standard types
- Access public endpoints
- Use basic data types (string, number, etc.)

### Registered Account
- Advanced types (name, address, etc.)
- Private endpoints with authentication
- Custom delays and HTTP codes
- Usage tracking

## 🤝 Contributing

We welcome contributions to improve MockFast documentation! Please see our [Contributing Guide](./CONTRIBUTING.md) for more information.

## 📞 Support

Need help? Reach out to us:

- [Documentation Issues](https://github.com/username/mockfast-docs/issues)
- [Visit MockFast.io](https://mockfast.io)
- [Buy Me a Coffee](https://ko-fi.com/mockfast)

## ⭐ Show Your Support

If MockFast has been helpful to you, please consider:
- Giving this repo a star ⭐
- Sharing feedback on our website
- Supporting the project by buying us a coffee

## 📜 License

This documentation is licensed under [MIT License](./LICENSE).

---

<p align="center">
  <a href="https://mockfast.io">MockFast.io</a> • 
  <a href="https://mockfast.io/documentation">Documentation</a> • 
  <a href="https://mockfast.io/roadmap">Roadmap</a>
</p>
