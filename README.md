# Sock Shop Integration Testing Assignment

## 🚀 Overview
This project demonstrates running the Sock Shop microservices application using Docker Compose and validating service interactions through integration testing.

---

## ✅ Output 1: Understanding of the Problem

The goal is to run a microservices-based application and verify that multiple services (catalogue, cart, user, etc.) work together correctly through integration testing.

---

## ✅ Output 2: Technical Approach

- Set up the Sock Shop application using Docker Compose
- Verified all services are running and accessible
- Performed API-based integration testing using curl
- Simulated real user flows:
  - Fetching products
  - Adding items to cart
  - Verifying cart data

---

## 🧪 Integration Tests

### 1. Fetch Catalogue
```bash
curl http://localhost/catalogue

2. Add Item to Cart (Session-based)
curl -c cookies.txt http://localhost

curl -b cookies.txt -c cookies.txt \
-X POST http://localhost/cart \
-H "Content-Type: application/json" \
-d '{"id":"03fef6ac-1896-4ce8-bd69-b798f85c6e0b"}'
3. Verify Cart
curl -b cookies.txt http://localhost/cart
🔑 Key Insight

The cart service depends on session-based cookies.
Integration tests must persist cookies across requests to simulate real user behavior.

🤖 Vibe Coding Evaluation
~70% of the task (setup, API testing, writing test flows) can be completed using AI tools
~30% requires human reasoning (debugging session handling, understanding service interactions)
📊 Patterns Identified
Microservices communication
API-driven architecture
Real-world debugging scenarios
Session-based workflows
🛠 Suggested Improvements
Add debugging scenarios (like session issues)
Include edge cases in test design
Separate AI-assisted vs logic-heavy tasks
🚀 Future Improvements
Automate tests using Jest or Supertest
Integrate tests into CI/CD pipeline

---

# ✅ After updating

Run:

```bash
git add README.md
git commit -m "Updated README - final submission"
git push
