# CrowdTangle-New-Actor-Searching-Algorithm

## Goal: 
Given a list of actors, we want to search and identify new actors (i.e. groups or pages) that are (or might be) part of the information network through certain behevaiors, i.e., link sharing, comments, messages, post description etc.

## Top level overview of the algorithm:
1.	The algorithm begins with already ingested CrowdTangle data associated with a list (either pages or groups).
2.	It then identifies the list of unique actors and most shared links.
3.	Afterwards by, using the /posts/search endpoint of CrowdTangle API, the algorithm searches the entire CrowdTangle database, where the most shared links are used as string inputs. Hence, it retrieves all posts that are connected to these most shared links or URLs (either via share, comment, description etc.).
4.	Algorithm then filters out and saves only the new actors, i.e., which were not present in the primary list.
5.	The algorithm then categorizes/classifies the newly found pages/groups into “media” or “news” pages/groups – by applying simple “heuristics” or rules. If the page/group name contains phrases like “News” or “Media” or “khabar”, then those pages/groups are identified under Media category.  
6.	The newly found actors (i.e., groups or pages) are then bulk uploaded to the CrowdTangle dashboard via a CSV file under new lists. 
