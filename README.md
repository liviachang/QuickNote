# QuickNote

## Anaconda
- Python version:
    - How to update python in Anaconda: `conda update python`
    - How to install a specific version of Python: `conda install python=3.6`


## Recommender
- Quick guide for collaborative filtering
    - [Towards Data Sciecne.com](https://towardsdatascience.com/various-implementations-of-collaborative-filtering-100385c6dfe0)


## Python package
- Impala Access
    ```python
    tmp = run_impala_query_to_csv(qq, '/tmp/tmp.csv', '', '', is_query_a_file=False)
    # [Error msg] AttributeError: 'TSocket' object has no attribute 'isOpen'
    # [Reference] https://stackoverflow.com/questions/46573180/impyla-0-14-0-error-tsocket-object-has-no-attribute-isopen
    # [Solution] 
        pip uninstall thrift-sasl
        pip uninstall impyla
        pip uninstall thrift

        pip install thrift-sasl==0.2.1 
        pip install thrift==0.9.3
        pip install impyla==0.13.8
    ```

- Regular expression replace
    ```python
    pdesc['stylecolor'] = pdesc['sku'].apply(lambda x: re.sub(r'(\d+)-(\w+)-(\w+)', r'\1-\2', x))
    ```
