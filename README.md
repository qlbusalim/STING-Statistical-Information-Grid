# STING-Statistical-Information-Grid

This repository implements the STING (Statistical Information Grid) algorithm, a method used in spatial data mining for efficient and scalable analysis of large datasets. The STING algorithm organizes spatial data into a hierarchical grid structure and uses statistical information stored in each cell to efficiently perform clustering and other data mining tasks. This approach allows for rapid queries and analysis, making it suitable for applications involving very large spatial databases.

## How STING Works (Based on Wang et al., 1997)

STING (Statistical INformation Grid), as introduced by Wei Wang, Jiong Yang, and Richard Muntz in 1997, is designed for scalable spatial data mining using the following principles:

- **Hierarchical Grid Structure:**  
  The spatial area is divided into rectangular cells at multiple levels of resolution, forming a hierarchical grid. Each cell at a higher level (coarser resolution) contains several cells at the next lower level (finer resolution).

- **Statistical Information Storage:**  
  Each cell in the grid stores statistical information about the objects it contains, including:
  - Number of objects
  - Mean and standard deviation of attributes
  - Minimum and maximum values
  - Other aggregate data

- **Query Processing:**  
  Queries (such as clustering or region queries) are processed top-down:
  1. **Filtering:** Irrelevant cells are filtered out at each level using stored statistics.
  2. **Drilling Down:** Only relevant cells are examined recursively down to finer resolutions.
  3. **Efficiency:** Most data can be ignored for each query, enabling high speed.

- **Clustering:**  
  Clusters are identified by grouping adjacent cells with statistics that meet certain criteria, allowing for fast discovery of dense regions.

- **Advantages:**  
  - High scalability for large datasets
  - Fast query response
  - Flexible for various spatial mining tasks

### Reference
Wang, W., Yang, J., & Muntz, R. (1997). STING: A Statistical Information Grid Approach to Spatial Data Mining. Proceedings of the 23rd International Conference on Very Large Data Bases (VLDB), pp. 186-195.

## Features

- Hierarchical grid-based spatial data representation
- Efficient clustering and statistical analysis of spatial data
- Suitable for large-scale datasets

## Usage

Clone the repository and follow the instructions in the source code to run the STING algorithm on your spatial data.

## License

This project is licensed under the terms of the repository's license.
