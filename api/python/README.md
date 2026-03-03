# Apache Arrow Python API Reference

This directory contains comprehensive API reference documentation for PyArrow (Apache Arrow Python).

## Files Created

1. **array.mdx** - Array classes and functions
   - Array base class and typed arrays (Int64Array, StringArray, etc.)
   - ChunkedArray for multi-chunk data
   - Array creation functions (array, chunked_array, nulls, repeat, concat_arrays)
   - Array methods (slice, cast, to_pylist, to_numpy)

2. **table.mdx** - Table and RecordBatch classes
   - Table for tabular data with chunked columns
   - RecordBatch for equal-length arrays
   - Table operations (filter, select, slice, sort_by, group_by)
   - Conversion methods (to_pandas, to_pydict)
   - RecordBatchReader for streaming

3. **schema.mdx** - Schema, Field, and DataType classes
   - Schema definition and manipulation
   - Field objects with names and types
   - All Arrow data types (primitives, temporal, nested, decimal)
   - Type utilities (unify_schemas, infer_type, from_numpy_dtype)

4. **compute.mdx** - Compute functions
   - Arithmetic operations (add, subtract, multiply, divide, power)
   - Aggregations (sum, mean, min, max, count, variance, stddev)
   - String functions (upper, lower, match_substring, replace_substring)
   - Filtering and selection (filter, take, index)
   - Sorting and ranking (sort_indices, top_k_unstable)
   - Type conversions (cast)
   - Null handling (is_null, is_valid, fill_null)
   - Comparison and logical operations
   - Expression API for complex queries

5. **dataset.mdx** - Dataset API for large data
   - Dataset creation and reading
   - FileSystemDataset for file-based datasets
   - Scanner for filtered/projected reads
   - Partitioning schemes (Directory, Hive, Filename)
   - Writing datasets (write_dataset)
   - File formats (Parquet, IPC, CSV, JSON, ORC)
   - Expression-based filtering

6. **filesystem.mdx** - Filesystem abstraction
   - FileSystem base class
   - LocalFileSystem for local storage
   - S3FileSystem for Amazon S3
   - GcsFileSystem for Google Cloud Storage
   - AzureFileSystem for Azure Blob Storage
   - HadoopFileSystem for HDFS
   - SubTreeFileSystem for path prefixes
   - FileInfo and FileSelector for file operations
   - Utility functions (copy_files)

## Documentation Features

Each file includes:
- Clear titles and descriptions in frontmatter
- Comprehensive function signatures with all parameters
- ParamField components for parameters with types and descriptions
- ResponseField components for return values
- Code examples demonstrating usage
- Coverage of both basic and advanced features
- Proper type annotations from the source code

## Source Code Analysis

The documentation was created by analyzing:
- `/home/daytona/workspace/source/python/pyarrow/__init__.py` - Main package exports
- `/home/daytona/workspace/source/python/pyarrow/compute.py` - Compute functions
- `/home/daytona/workspace/source/python/pyarrow/dataset.py` - Dataset API
- `/home/daytona/workspace/source/python/pyarrow/fs.py` - Filesystem API
- Cython source files (.pxi) for core classes

All class definitions, method signatures, and docstrings were extracted from the actual Apache Arrow Python source code to ensure accuracy and completeness.
