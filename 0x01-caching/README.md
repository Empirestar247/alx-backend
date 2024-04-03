# 0x01-caching

## Cache Algorithms Implementation

This project implements various caching algorithms in Python. Caching is a technique used in computer science to store frequently accessed data in a fast-accessible memory location to reduce the time complexity of operations. This project explores different caching algorithms such as FIFO, LIFO, LRU, MRU, and LFU.

## Table of Contents
- [General Information](#general-information)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [How to Use](#how-to-use)
- [Implementation Details](#implementation-details)
- [Contributing](#contributing)
- [License](#license)

## General Information

In this project, we've implemented the following caching algorithms:

- **BasicCache**: A basic caching system that doesn't have a limit on the number of items stored.
- **FIFOCache**: FIFO (First In, First Out) caching algorithm, where the least recently used item is removed when the cache is full.
- **LIFOCache**: LIFO (Last In, First Out) caching algorithm, where the most recently added item is removed when the cache is full.
- **LRUCache**: LRU (Least Recently Used) caching algorithm, where the least recently accessed item is removed when the cache is full.
- **MRUCache**: MRU (Most Recently Used) caching algorithm, where the most recently accessed item is removed when the cache is full.
- **LFUCache**: LFU (Least Frequently Used) caching algorithm, where the least frequently accessed item is removed when the cache is full.

## Technologies Used

- Python 3.7
- pycodestyle (for code style enforcement)

## Project Structure

The project directory is structured as follows:

```
0x01-caching/
│
├── base_caching.py
├── 0-basic_cache.py
├── 1-fifo_cache.py
├── 2-lifo_cache.py
├── 3-lru_cache.py
├── 4-mru_cache.py
└── 5-lfu_cache.py
```

## How to Use

To use any of the implemented caching algorithms, you can instantiate the respective class and use the `put` and `get` methods:

```python
# Example usage of LRUCache

from 3-lru_cache import LRUCache

my_cache = LRUCache()
my_cache.put("A", "Hello")
my_cache.put("B", "World")
my_cache.put("C", "Holberton")

print(my_cache.get("A"))  # Output: Hello
print(my_cache.get("D"))  # Output: None
```

## Implementation Details

- Each caching algorithm is implemented as a separate Python class that inherits from the `BaseCaching` class.
- The `BaseCaching` class provides basic functionalities and abstract methods that must be implemented by the derived caching classes.
- The algorithms follow the specified eviction policies when the cache is full, either discarding the least recently used item, most recently used item, or least frequently used item, depending on the algorithm.

## Contributing

Contributions are welcome! If you have any suggestions, improvements, or new features to add, feel free to open an issue or create a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
