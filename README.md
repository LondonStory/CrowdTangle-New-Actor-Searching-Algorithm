# CrowdTangle-New-Actor-Searching-Algorithm

1. The algorithm begins with an already ingested CrowdTangle data associated with a list (either pages or groups). 
2. It then identifies the list of unique actors and most shared links. 
3. Afterwards by using the /posts/search endpoint of CrowdTangle, the algorithm searches the entire CrowdTangle database, where the most shared links are used as inputs. Hence, it retrieves all posts that are connected to these most shared links or URLs (either via share, comment, description etc.)
4. Algorithm then filters out and saves only the new actors, i.e., which were not present in the primary dataset.
5. The newly found actors (i.e., groups or pages) are then bulk uploaded to the CrwodTangle dashboard under a new list. 
