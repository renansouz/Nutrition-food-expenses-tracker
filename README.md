# Personal Nutrition & Food Expense Tracker

Product Documentation

## 1. Overview

The Personal Nutrition & Food Expense Tracker is a web application designed to help individuals track their food consumption, nutritional intake, and daily food expenses. The system allows users to register food products they purchase, record meals throughout the day, and automatically calculate nutritional values and costs associated with each meal.

The primary objective of the application is to provide a structured way to manage a personal diet routine while also understanding how much money is spent on food and how well the user's nutrition aligns with their health goals.

The system will store food data in a database and use it to calculate daily, weekly, and long-term insights about diet quality, nutrient intake, and financial cost.

Future versions of the system may integrate artificial intelligence to assist with personalized nutrition planning and food recommendations.

---

# 2. Core Objectives

The application aims to:

* Organize all purchased food items in a structured database.
* Record meals consumed throughout the day.
* Automatically calculate nutrient intake based on meal composition.
* Track food spending per meal and per day.
* Compare nutritional intake against user-defined health goals.
* Display visual analytics that help users understand their eating habits.

---

# 3. Key Features

## 3.1 Food Registration

Users can register any food item they purchase from a supermarket or other source.

Each food entry includes:

* Food name
* Brand (optional)
* Nutritional information per 100 grams
* Purchase price
* Total weight purchased
* Purchase date
* Store name (optional)

This information will be stored in the database and reused when building meals.

### Example

User buys:

* 1 kg of rice for R$15

Nutrition label per 100 g:

* Carbohydrates: 24 g
* Protein: 1.4 g
* Fat: 0.2 g

The system will store both nutritional values and purchase data.

This enables the system to calculate:

* Nutrition consumed
* Cost of each portion

---

# 4. Meal Management

Users will create meals during the day using foods previously registered in the system.

The default meal categories are:

* Breakfast
* Lunch
* Snack
* Dinner

Each meal can contain multiple food items with a specific weight.

### Example Meal (Lunch)

* 100 g Rice
* 200 g Chicken
* 200 g Beans

For each item, the system will automatically calculate:

* Carbohydrates
* Protein
* Fat
* Calories
* Cost of the portion

All values will be summed to generate the total for the meal.

---

# 5. Daily Summary

At the end of the day the system calculates the total nutritional intake and cost.

Daily totals include:

* Total calories
* Total protein
* Total carbohydrates
* Total fat
* Total fiber (optional)
* Total money spent on food

The application will also provide a breakdown by meal.

Example:

Daily Nutrition Summary

Breakfast
Lunch
Snack
Dinner

Total Daily Intake

---

# 6. Health Indicators

The system will allow users to store personal health information in order to evaluate their diet.

User profile data may include:

* Height
* Weight
* Age
* Activity level

Using this information the application can calculate:

## BMI (Body Mass Index)

BMI = weight (kg) / height² (meters)

The BMI result will help evaluate the user's current health status.

---

# 7. Nutritional Goals

Users will define personal nutrition goals such as:

* Daily calorie target
* Daily protein target
* Daily carbohydrate target
* Daily fat target

The system will compare:

Actual intake vs Target intake.

Example feedback:

* Protein goal: 120 g
* Consumed: 95 g
* Completion: 79%

This helps the user understand whether their diet supports their goals.

---

# 8. Data Visualization

The application will include visual analytics dashboards.

Possible charts include:

### Nutrition Distribution

Pie chart showing percentage of:

* Protein
* Carbohydrates
* Fat

### Daily Spending

Bar chart showing food expenses per day.

### Goal Progress

Charts comparing consumed nutrients with target values.

### Historical Trends

Graphs showing changes in diet and spending over time.

---

# 9. Data Storage

The system will maintain structured data using a relational database.

Main data entities include:

### Users

Stores personal account information.

### Food Items

Stores nutritional data for each food product.

### Purchases

Stores price and quantity information when foods are bought.

### Meals

Represents a meal event on a specific date.

### Meal Items

Stores foods and quantities included in each meal.

### Nutrition Goals

Stores daily nutrition targets defined by the user.

---

# 10. Example Cost Calculation

If a user buys:

1 kg of rice for R$15

Cost per gram:

15 / 1000 = R$0.015 per gram

Cost for 100 g:

0.015 × 100 = R$1.50

If a meal contains:

100 g rice
200 g chicken
200 g beans

The system calculates the cost of each portion and sums them to obtain the total meal cost.

---

# 11. User Interface Pages

The application will contain the following main sections.

### Dashboard

Shows daily nutrition totals and meal summaries.

### Food Library

Allows users to view, edit, and add foods to the database.

### Food Registration Form

Form for entering nutritional information and purchase data.

### Meal Planner

Interface where users add foods to breakfast, lunch, snacks, and dinner.

### History

Calendar or list view showing past days and meals.

### Analytics

Visual charts showing nutrition patterns and spending trends.

### Settings

User profile information and nutrition goals.

---

# 12. Future AI Features

Although artificial intelligence is not required in the initial version, the system architecture will allow future integration.

Possible AI features include:

* Automatic meal suggestions
* Diet optimization based on goals
* Nutrition deficiency detection
* Personalized grocery list recommendations
* Cost-efficient meal planning
* Pattern detection in eating habits

These features may use historical data stored by the system.

---

# 13. Minimum Viable Product (MVP)

The first version of the application should include:

1. User account system
2. Food registration form
3. Meal creation and editing
4. Automatic nutrition calculations
5. Daily summary page
6. Cost tracking per meal
7. Basic analytics charts

Once the MVP is stable, additional features and AI integration can be added.

---

# 14. Long-Term Vision

The long-term goal is to create a personal nutrition intelligence system that helps users:

* Maintain healthy eating habits
* Understand their food spending
* Optimize diet quality
* Make data-driven nutrition decisions

With sufficient data, the platform could evolve into an intelligent diet assistant capable of providing personalized recommendations and predictive insights.


# Production-ready Full-Stack

- Backend language: Python
- Backend framework: FastAPI
- ORM & migrations: SQLAlchemy + Alembic
- Authentication: JWT (via FastAPI)
- Frontend: React + TypeScript
- Styling: Tailwind CSS
- Data fetching / cache: TanStack Query
- Database & storage: PostgreSQL hosted on Supabase
- Caching / broker: Redis (provider: Upstash)
- Containerization: Docker
- CI / CD & VCS: GitHub (use Actions)
- Frontend hosting: Vercel
- Backend hosting: Render
- Testing: pytest and Jest
- Monitoring: Sentry
