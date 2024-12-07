# Article Management System
This Python Challenge defines a set of classes to model the relationships between authors, articles, and magazines. It allows managing articles and their associated authors and magazines. The key feature of this system is its structure, where each Article is associated with an Author and a Magazine, with validation rules for each entity. Additionally, it provides methods for managing and querying articles, authors, and magazines.

# Class Overview
1. Article Class
The Article class represents an article published in a magazine, with the following attributes:

author: An instance of the Author class.
magazine: An instance of the Magazine class.
title: A string representing the article's title. The title has a length constraint of between 5 and 50 characters.
The Article class has the following functionality:

Validation of the article's title when setting it (ensuring it is a string and meets the length requirement).
Ensuring the associated author is an instance of the Author class.
Ensuring the associated magazine is an instance of the Magazine class.
A class-level list all that holds all instances of Article.
2. Author Class
The Author class represents an author who can write articles for different magazines, with the following attributes:

name: The name of the author. The name must be a string and cannot be changed once set.
The Author class has the following functionality:

Validation of the author's name when setting it (ensuring it is a non-empty string).
Methods to:
Retrieve all articles written by the author.
Retrieve all magazines the author has contributed to.
Add a new article for the author in a specific magazine.
Retrieve a list of topic areas the author has written about (derived from the categories of the magazines they have contributed to).
3. Magazine Class
The Magazine class represents a magazine, which can contain multiple articles, with the following attributes:

name: The name of the magazine, constrained to be between 2 and 16 characters.
category: The category or genre of the magazine (e.g., Technology, Science, etc.).
The Magazine class has the following functionality:

Validation of the magazine's name and category when setting them.
Methods to:
Retrieve all articles published in the magazine.
Retrieve a list of contributors (authors) who have written articles for the magazine.
Retrieve a list of all article titles in the magazine.
Retrieve a list of authors who have contributed more than once to the magazine.
Example Usage
Here's how you can use the system:

python
Copy code
# Create an author
john = Author("John Doe")

# Create a magazine
tech_mag = Magazine("Tech Monthly", "Technology")

# Add an article written by John in Tech Monthly
article1 = john.add_article(tech_mag, "The Future of AI")

# Retrieve and display articles written by John
print(john.articles())  # Lists articles by John

# Retrieve and display magazines John has contributed to
print(john.magazines())  # Lists magazines John contributed to

# Retrieve and display articles in Tech Monthly
print(tech_mag.articles())  # Lists articles in "Tech Monthly"

# Retrieve and display contributors to Tech Monthly
print(tech_mag.contributors())  # List of authors who contributed to the magazine
Features and Constraints
Article Constraints:
Title must be a string between 5 and 50 characters.
Once set, the title cannot be changed.
An article must be associated with both an Author and a Magazine.
Author Constraints:
Name must be a string.
The author's name cannot be changed once set.
The author can add articles to magazines and retrieve their contributions.
Magazine Constraints:
Name must be between 2 and 16 characters.
Category must be a non-empty string.
A magazine can list its articles, contributors, article titles, and identify authors who have contributed more than once.
Error Handling
The code includes error handling for the following situations:

Title of an article: Must be a string and within the specified length constraints (5–50 characters).
Author of an article: Must be an instance of the Author class.
Magazine of an article: Must be an instance of the Magazine class.
Name of an author or magazine: Must meet the specified constraints for length and type.
Extending the System
This system can be easily extended to include additional features such as:

Adding more validation rules.
Supporting multiple categories for magazines.
Allowing authors to collaborate on articles.
Providing advanced querying features for articles, authors, and magazines.
Feel free to contribute to the development of this system to better manage articles, authors, and magazines!

