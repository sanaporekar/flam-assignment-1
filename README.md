# flam-assignment-1
Android assignment set -1 // SANA POREKAR MNNIT- 20214296

table of content :
1. LRU Cache
2. Implementing HashMap
3. Book Review App (MVP)

LRU CACHE :
Implements an LRU (Least Recently Used) Cache with get(key) and put(key, value) in O(1) time complexity using a combination of hash map and doubly linked list.
key components -
Doubly Linked List: for tracking the order of usage
HashMap : for O(1) access to the nodes

Implementing HashMap:
Implements a simplified HashMap with constant-time average case operations for put, get, and remove without using STL hash maps.
key design -
Uses an array of size 1000001 to simulate hash buckets.
Direct addressing used since key range is known.

Book Review App :
Build a Book Review Android App (Java) using Clean Architecture (or MVVM). Supports online browsing and offline saving (favorites).

Architecture:
Domain Layer: Entities, UseCases, Repositories
Data Layer: Room (SQLite) and Retrofit (Fake API)
Presentation Layer: ViewModels and Activities

Technologies-
Java (No Kotlin)
Retrofit (API)
Room (SQLite DB)
LiveData (Reactive UI)
No third-party image libraries

Domain Layer

Book.java - Model

GetBooks.java - UseCase to fetch books

SaveFavorite.java - UseCase to save favorite

BookRepository - Interface

Data Layer

BookEntity, BookDao, BookDatabase

ApiService - Retrofit interface

BookRepoImpl - Implements Repository using DAO + API

Presentation Layer

BookListVM.java, BookDetailVM.java - ViewModels

BookListActivity.java, BookDetailActivity.java - UI

Sample Flow :

Open BookList → API fetches books → UI updates via LiveData

Click on book → Navigate to Detail screen

Click favorite → Book saved in Room → Can view later offline
