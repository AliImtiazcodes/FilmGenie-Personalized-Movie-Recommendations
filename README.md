# FilmGenie-Personalized-Movie-Recommendations
FilmGenie is a Java-based movie recommendation system using Swing GUI, offering personalized suggestions based on age, gender, region, and genre. It features a dark-themed UI, instant feedback, and dynamic data handling. Built with OOP principles (Encapsulation, Abstraction, Inheritance, Polymorphism), it ensures a smart and interactive experience.

## Features

### Personalized Movie Recommendations
- Users receive tailored movie suggestions based on their input.
- The system considers **age, gender, region, and preferred genres** to filter recommendations.

### Interactive GUI
- **Swing-based graphical user interface** for an engaging user experience.
- Dark-themed layout with clear and well-structured components.

### Dynamic Search & Filtering
- Users can **search movies** dynamically.
- Filters allow users to refine suggestions.

### Instant Feedback System
- Displays immediate feedback based on user selections.
- Helps users find movies they’ll likely enjoy.

### Data Handling
- Stores and processes user preferences efficiently.
- Retrieves movie details dynamically.

### Restartable & Reset Options
- Users can reset their preferences and start fresh without restarting the program.

---

## OOP Concepts Used

- **Encapsulation**: User data and preferences are handled through private attributes and accessed via getters/setters.
- **Abstraction**: Complex data handling and filtering logic are encapsulated within classes.
- **Inheritance**: The system follows a hierarchical structure with base and derived classes for different components.
- **Polymorphism**: Methods are overridden to handle different user input cases effectively.

---

## Java Concepts Used

### **Classes & Objects**
- **User Class**: Stores user details (age, gender, region, genre preference).
- **Movie Class**: Holds movie details such as title, genre, and rating.
- **RecommendationEngine Class**: Implements the recommendation logic.

### **Functions & Methods**

#### **displayGUI()**
- Initializes the **Swing-based GUI** and displays components.

```java
public void displayGUI() {
    JFrame frame = new JFrame("FilmGenie - Movie Recommendations");
    frame.setSize(500, 500);
    frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    frame.setLayout(new BorderLayout());
    
    JLabel title = new JLabel("Welcome to FilmGenie");
    frame.add(title, BorderLayout.NORTH);
    
    frame.setVisible(true);
}
```

#### **getRecommendations()**
- Generates movie recommendations based on user input.

```java
public List<Movie> getRecommendations(User user) {
    List<Movie> filteredMovies = new ArrayList<>();
    for (Movie movie : movieDatabase) {
        if (movie.matchesPreferences(user)) {
            filteredMovies.add(movie);
        }
    }
    return filteredMovies;
}
```

#### **handleUserInput()**
- Processes user preferences and updates the recommendation list.

```java
public void handleUserInput() {
    User user = new User(age, gender, region, genre);
    List<Movie> recommendations = getRecommendations(user);
    displayMovies(recommendations);
}
```

---

## Example Interaction

```plaintext
-----------------------------------
Welcome to FilmGenie
-----------------------------------

Enter your age: 21
Select your gender (M/F): M
Choose your region: Hollywood
Select your preferred genre: Action

Recommended Movies:
1. Mad Max: Fury Road
2. John Wick
3. The Dark Knight
```

## Conclusion
**FilmGenie** is a dynamic and engaging movie recommendation system that demonstrates key **OOP principles**, GUI handling using **Swing**, and efficient **data filtering**. The project enhances user interaction and ensures a smooth recommendation experience while leveraging Java's powerful capabilities for building interactive applications.

 

