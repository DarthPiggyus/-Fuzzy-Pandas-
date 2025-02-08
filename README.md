#This code will give you a consolidated view of the genre counts across all three genre columns and sort them in descending order to show the most common genres.
#frist part is good 

# Concatenate the genre groups
combined_genre_group = pd.concat([genre1_group, genre2_group, genre3_group])

# Group by genre and sum the counts
combined_genre_group = combined_genre_group.groupby('Genre')['Count'].sum().reset_index()

# Sort by count in descending order
combined_genre_group = combined_genre_group.sort_values(by='Count', ascending=False)

# Display the result
display(combined_genre_group)
