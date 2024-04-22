# Pagination Readme

## Table of Contents
- [Pagination Readme](#pagination-readme)
  - [Table of Contents](#table-of-contents)
  - [Pagination with Simple Page and Page\_Size Parameters](#pagination-with-simple-page-and-page_size-parameters)
  - [Pagination with Hypermedia Metadata](#pagination-with-hypermedia-metadata)
  - [Pagination in a Deletion-Resilient Manner](#pagination-in-a-deletion-resilient-manner)
    - [**Authors**](#authors)

---

## Pagination with Simple Page and Page_Size Parameters
Pagination is a common technique for dividing a large dataset into smaller, more manageable chunks. Here's how to paginate a dataset using simple `page` and `page_size` parameters:

1. **Parameters**: Define two parameters, `page` and `page_size`, to control the pagination process. `page` indicates the current page, while `page_size` sets the number of items per page.

2. **Calculate Offsets**: Calculate the offset for the current page by multiplying `(page - 1)` by `page_size`. This offset helps skip items from previous pages.

3. **Retrieve Data**: Use the calculated offset and `page_size` to fetch the relevant subset of data from your dataset.

4. **Display Data**: Display the retrieved data to the user. This chunk represents one page of results.

5. **Navigation**: Provide options for users to navigate between pages, typically through "next page" and "previous page" buttons. Ensure that you update the `page` parameter accordingly.

## Pagination with Hypermedia Metadata
Hypermedia-driven pagination involves including metadata within the API response to guide clients on how to paginate effectively. Here's how to implement pagination with hypermedia metadata:

1. **Include Metadata**: Alongside the paginated data, include metadata that provides information about the current page, total number of pages, and links to navigate to other pages.

2. **Metadata Structure**: Common metadata fields include `current_page`, `total_pages`, `total_items`, `page_size`, `next_page`, and `prev_page`. The `next_page` and `prev_page` fields contain links to the next and previous pages.

3. **Client Interaction**: Clients can inspect the metadata to understand the pagination structure and decide how to request the next or previous pages dynamically.

4. **Flexible Navigation**: This approach allows for more flexible navigation as clients can adapt to changes in the dataset size and structure.

## Pagination in a Deletion-Resilient Manner
Handling deletions while paginating requires additional considerations to ensure a smooth user experience:

1. **Stable Page Size**: Maintain a stable `page_size` throughout the pagination process, even as items are deleted. If items are deleted from the current page, replace them with new items to maintain the specified `page_size`.

2. **Adjust Page Number**: If an item deletion results in a current page with fewer items than the specified `page_size`, consider reducing the `page` parameter to navigate to the next page appropriately.

3. **Metadata Updates**: Update hypermedia metadata to reflect the changes. Ensure that the metadata accurately represents the current state of the dataset, including the adjusted page number and total pages.

4. **Consistency**: Aim for a consistent user experience where deletions do not disrupt the pagination flow. Users should be able to navigate through the dataset seamlessly, even if items are removed.

---


### **Authors**
--- 

![GitHub Contributors Image](https://contrib.rocks/image?repo=RM92023/holbertonschool-low_level_programming)
Robinson Muñetón Jaramillo - <a href="https://github.com/RM92023" target="_blank"> @RM92023</a> ![Your Repository's Stats](https://github-readme-stats.vercel.app/api?username=RM92023&show_icons=true)
