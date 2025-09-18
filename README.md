import pandas as pd

data = pd.read_csv("/Users/michaeljeon/Downloads/dataset.csv")

clean_data = data.drop(['index', 'track_id', 'album_name', 'danceability', 
                        'key', 'loudness', 'mode', 'speechiness', 'acousticness', 'instrumentalness', 'liveness', 'valence', 'tempo', 'time_signature'], axis=1)

sorted_data = clean_data.sort_values(by='popularity', ascending=False)

print(sorted_data.head(10))
