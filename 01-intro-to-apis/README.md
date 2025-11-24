# **Introduction to APIs**

An **API (Application Programming Interface)** is a set of rules and protocols that allows different software applications to communicate with each other.

APIs define the **methods**, **data formats**, and **standards** that applications can use to request and exchange information.

They are essential for enabling **integration** between different systems, allowing developers to build applications that can leverage the functionality of other services and platforms.

---

# **How an API Works**

A simple way to understand how an API works is to look at an example such as third-party payment processors (e.g., PayPal, Stripe) integrated into e-commerce websites.

When a user makes a purchase on an e-commerce site, the site uses the payment processor’s API to securely handle the transaction.

1. The user initiates a payment on the e-commerce site.
2. The e-commerce site sends a request to the payment processor’s API with the payment details.
3. The payment processor processes the payment and sends a response back to the e-commerce site indicating whether the payment was successful or failed.
4. The e-commerce site then updates the user with the payment status.

<img width="1200" height="600" alt="image" src="https://github.com/user-attachments/assets/cf98b2e7-04e0-47b1-9548-e8fdf151a27f" />

---

# **Types of APIs**

APIs can be categorized into different types based on their usage and accessibility:

<img width="746" height="419" alt="image" src="https://github.com/user-attachments/assets/9dc0e65a-4745-45e7-a936-707d569e83c8" />

1. **Open APIs (Public APIs)**:
   These are available to developers and other users with minimal restrictions.
   Intended for **external users**.
   **Examples:** Twitter API, Google Maps API.

2. **Internal APIs (Private APIs)**:
   Used within an organization to connect internal systems and services.
   Not exposed to external users.
   **Example:** APIs used for communication between HR, payroll, and finance systems.

3. **Partner APIs**:
   Shared with specific business partners.
   Usually require authentication, agreements, or licenses.
   **Example:** A shipping company providing an API to e-commerce platforms for order tracking.

4. **Composite APIs**:
   Combine multiple API calls into a single call.
   Useful for reducing the number of client requests and improving performance.
   **Example:** An API that aggregates data from multiple microservices to provide a unified response (e.g., combining weather data from multiple sources).

---

APIs play a crucial role in modern software development, enabling **interoperability**, **scalability**, **enhanced functionality**, and **innovation** across various applications and services.

---

# **API vs SDK**

**API (Application Programming Interface)** and **SDK (Software Development Kit)** are essential tools in the software development world, but they serve distinct purposes:

## **API:**

An **API** is a set of rules and protocols that allows different software applications and services to communicate with each other.

* It defines **how software components should interact**.
* Facilitates **data exchange** and **functionality access** between software components.
* Typically consists of **endpoints**, **requests**, and **responses**.

## **SDK:**

An **SDK** is a comprehensive package of **tools**, **libraries**, **sample code**, and **documentation** that assists developers in building applications for a particular platform, framework, or hardware.

* Offers **higher-level abstractions**, simplifying development for a specific platform.
* Tailored to **specific platforms or frameworks**, ensuring compatibility and optimal performance.
* Provides access to **advanced features and capabilities** specific to the platform, which might be otherwise challenging to implement from scratch.

The choice between APIs and SDKs depends on the **development goals** and **requirements** of the project.

In simple terms:

* An **API** is a **set of rules for communication** between software components.
* An **SDK** is a **complete toolkit** that includes APIs and other resources to facilitate application development on a specific platform.

---

Part 2 : [HTTP and Terminology](/02-http-and-terminology/)
