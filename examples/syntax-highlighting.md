---
marp: true
theme: mischok-academy
class: title
---

# Syntax-Highlighting Test
## mischok-academy Theme

---

<!-- _class: content -->

# JavaScript/TypeScript

```javascript
function fibonacci(n) {
  if (n <= 1) return n;
  return fibonacci(n - 1) + fibonacci(n - 2);
}

// Template literals
const message = `Hello ${name}!`;
const numbers = [1, 2, 3].map(x => x * 2);

// Modern syntax
const { data, loading } = useQuery(GRAPHQL_QUERY);
```

```typescript
interface User {
  id: number;
  name: string;
  email?: string;
}

class ApiClient<T> {
  async fetch(url: string): Promise<T> {
    const response = await fetch(url);
    return response.json();
  }
}
```

---

<!-- _class: content -->

# Python

```python
@dataclass
class Person:
    name: str
    age: int
    
    def greet(self) -> str:
        return f"Hello, I'm {self.name} and I'm {self.age} years old"

# List comprehension
squares = [x**2 for x in range(10) if x % 2 == 0]

# Context manager
with open('file.txt', 'r') as file:
    content = file.read()
```

---

<!-- _class: content -->

# CSS/SCSS

```css
.button {
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 4px;
  padding: 0.5rem 1rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.button:hover {
  background-color: #0056b3;
}

@media (max-width: 768px) {
  .button {
    width: 100%;
  }
}
```

```scss
$primary-color: #007bff;
$border-radius: 4px;

.button {
  background-color: $primary-color;
  border-radius: $border-radius;
  
  &:hover {
    background-color: darken($primary-color, 10%);
  }
  
  @include media-breakpoint-down(md) {
    width: 100%;
  }
}
```

---

<!-- _class: content -->

# HTML

```html
<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mischok Academy</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header class="main-header">
        <h1>Welcome to Mischok Academy</h1>
        <nav>
            <a href="#courses">Courses</a>
            <a href="#about">About</a>
        </nav>
    </header>
    
    <main>
        <section id="hero">
            <p>Learn coding with us!</p>
        </section>
    </main>
    
    <script src="app.js"></script>
</body>
</html>
```

---

<!-- _class: content -->

# Bash/Shell

```bash
#!/bin/bash

# Variables
PROJECT_DIR="/home/user/project"
LOG_FILE="deploy.log"

# Functions
function deploy() {
    echo "Starting deployment..." | tee -a $LOG_FILE
    
    cd $PROJECT_DIR || exit 1
    
    # Build the project
    npm run build
    
    if [ $? -eq 0 ]; then
        echo "Build successful!" | tee -a $LOG_FILE
        rsync -av dist/ server:/var/www/html/
    else
        echo "Build failed!" >&2
        exit 1
    fi
}

# Execute deployment
deploy
```

---

<!-- _class: content -->

# JSON

```json
{
  "name": "mischok-academy-theme",
  "version": "1.0.0",
  "description": "Professional Marp theme for Mischok Academy",
  "main": "mischok-academy.css",
  "scripts": {
    "build": "marp --theme ./mischok-academy.css slides.md",
    "dev": "marp --theme ./mischok-academy.css --watch slides.md"
  },
  "keywords": ["marp", "theme", "presentation", "academy"],
  "author": "Mischok Academy",
  "license": "MIT",
  "devDependencies": {
    "@marp-team/marp-cli": "^3.4.0"
  }
}
```

---

<!-- _class: content -->

# SQL

```sql
-- User management queries
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    username VARCHAR(50) UNIQUE NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    password_hash TEXT NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Complex query with JOIN
SELECT 
    u.username,
    COUNT(p.id) as post_count,
    AVG(p.rating) as avg_rating
FROM users u
LEFT JOIN posts p ON u.id = p.user_id
WHERE u.created_at > '2024-01-01'
GROUP BY u.id, u.username
HAVING COUNT(p.id) > 5
ORDER BY avg_rating DESC
LIMIT 10;
```

---

<!-- _class: closing -->

# Syntax-Highlighting ✅

Vollständig implementiert für das mischok-academy Theme!

**Unterstützte Sprachen:** JavaScript, TypeScript, Python, CSS/SCSS, HTML, Bash, JSON, SQL und viele weitere...