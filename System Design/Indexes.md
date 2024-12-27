Indexes are well known when it comes to databases, they are **==used to improve the speed of data retrieval operations on the data store.==** An index makes the trade-offs of increased storage overhead, and **slower writes** (since we not only have to write the data but also have to update the index) for the benefit of faster reads. Indexes are ==used to quickly locate data without having to examine every row in a database table.== Indexes can be created using one or more columns of a database table, providing the basis for both rapid random lookups and efficient access to ordered records.

Indexes can also organize data in different ways (like sorting or filtering) without duplicating it. There are two main types of indexes:

- **Dense indexes:** Have pointers for every row, so they use more space but are very precise.
- **Sparse indexes:** Have pointers for some rows, saving space but potentially slower to find data.