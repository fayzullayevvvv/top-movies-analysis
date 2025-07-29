# Import necessary libraries
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np

# Step 1: Load the dataset
df = pd.read_csv("movies.csv.txt")

# Step 2: Filter movies with rating >= 8
high_rated = df[df['Rating'] >= 8]

# Step 3: Save high-rated movies to a new CSV file
high_rated.to_csv("high_rated_movies.csv", index=False)

# Step 4: Plot movie ratings
plt.figure(figsize=(10, 5))
plt.plot(df['Title'], df['Rating'], marker='o', color='green')
plt.title("Movie Ratings")
plt.xlabel("Movie Title")
plt.ylabel("Rating")
plt.xticks(rotation=45)
plt.grid(True)
plt.tight_layout()
plt.show()

# Step 5: Plot number of movies by genre
genre_counts = df["Genre"].value_counts()

plt.figure(figsize=(8, 5))
plt.bar(genre_counts.index, genre_counts.values, color='skyblue')
plt.title("Number of Movies by Genre")
plt.xlabel("Genre")
plt.ylabel("Number of Movies")
plt.grid(axis='y')
plt.yticks(np.arange(0, genre_counts.max() + 1))
plt.tight_layout()
plt.show()
