# Detailed write-up for the spotlight challange E-Bazaar for the 2026 ISSessions FantasyCTF
<img width="914" height="417" alt="image" src="https://github.com/user-attachments/assets/2182e93f-d2bf-4b1c-ad0f-a4db56c515c9" />

The index page of the challange:
<img width="1618" height="1315" alt="image" src="https://github.com/user-attachments/assets/0fee0c15-8c6f-4828-8bcb-fd4dc885946d" />

By looking at the index page, we can understand that the goal is probably to purchase the items that seem unobtainable such as:
The "Iced out magic wand" and the "Elixir vitae"
<img width="630" height="112" alt="image" src="https://github.com/user-attachments/assets/1d572564-9c92-42e9-9805-ff2a5610ebb9" />

First, we check to see if there are any hidden routes so we visit common routes like /robots.txt /sitemap.xml /admin

Sure enough, /admin exists but we can't visit it yet
<img width="855" height="172" alt="image" src="https://github.com/user-attachments/assets/1d1021a3-022c-430d-9fef-c59f8b8219e4" />


In the challange description, it says to "piece together a 3 piece flag using different web exploits", so I know that I will need 3 pieces

I go back to the index page and check the source code and find something interesting:
<img width="600" height="502" alt="image" src="https://github.com/user-attachments/assets/3c85c146-0633-4684-8940-e77515f665a5" />

This tells me that there is a hidden item with the item id 6, so I must somehow try and purchase that item

I launch burpsuite to take a look at the HTTP response responsible for adding an item to the cart
