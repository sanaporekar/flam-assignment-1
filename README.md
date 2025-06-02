# flam-assignment-1
Android assignment set -1 // SANA POREKAR MNNIT- 20214296

table of content :
1. LRU Cache
2. Implementing HashMap
3. Book Review App (MVP)

LRU CACHE :
1. Implements an LRU (Least Recently Used) Cache with get(key) and put(key, value) in O(1) time complexity using a combination of hash map and doubly linked list.
2. key components -
1. Doubly Linked List: for tracking the order of usage
2. HashMap : for O(1) access to the nodes

Implementing HashMap :
1. Implements a simplified HashMap with constant-time average case operations for put, get, and remove without using STL hash maps.
2. key design -
1. Uses an array of size 1000001 to simulate hash buckets.
2. Direct addressing used since key range is known.

Book Review App :
1. Build a Book Review Android App (Java) using Clean Architecture (or MVVM). Supports online browsing and offline saving (favorites).

 Architecture:
1. Domain Layer: Entities, UseCases, Repositories
2. Data Layer: Room (SQLite) and Retrofit (Fake API)
3. Presentation Layer: ViewModels and Activities

 Technologies-
1. Java (No Kotlin)
2. Retrofit (API)
3. Room (SQLite DB)
4. LiveData (Reactive UI)
5. No third-party image libraries

 Domain Layer

1. Book.java - Model

2. GetBooks.java - UseCase to fetch books

3. SaveFavorite.java - UseCase to save favorite

4. BookRepository - Interface

 Data Layer

1. BookEntity, BookDao, BookDatabase

2. ApiService - Retrofit interface

3. BookRepoImpl - Implements Repository using DAO + API

Presentation Layer

1. BookListVM.java, BookDetailVM.java - ViewModels

2. BookListActivity.java, BookDetailActivity.java - UI

Sample Flow :

1. Open BookList → API fetches books → UI updates via LiveData

2. Click on book → Navigate to Detail screen

3. Click favorite → Book saved in Room → Can view later offline
