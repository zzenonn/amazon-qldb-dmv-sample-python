# Amazon QLDB Python DMV Sample App

The samples in this project demonstrate several uses of Amazon Quantum Ledger Database (QLDB).

For our tutorial, see [Python and Amazon QLDB](https://docs.aws.amazon.com/qldb/latest/developerguide/getting-started.python.html).

## Requirements

### Basic Configuration

See [Accessing Amazon QLDB](https://docs.aws.amazon.com/qldb/latest/developerguide/accessing.html) for information on connecting to AWS.

### Required Python versions

DMV Sample App v1.x requires Python 3.4 or later.

DMV Sample App v2.x requires Python 3.6 or later. 

Please see the link below for more detail to install Python:

* [Python Installation](https://www.python.org/downloads/)

## Installing the driver and dependencies

Install Python QLDB driver and other dependencies using pip:

```
pip install -r requirements.txt
```

## Running the Sample code

The sample code creates a ledger with tables and indexes, and inserts some documents into those tables,
among other things. Each of the examples in this project can be run in the following way:

```python
python create_ledger.py
```

The above example will build the CreateLedger class with the necessary dependencies and create a ledger named:
`vehicle-registration`. You may run other examples after creating a ledger.

## Documentation

Sphinx is used for documentation. You can generate HTML locally with the following:

```
$ pip install -r requirements-docs.txt
$ pip install -e .
$ cd docs
$ make html
```

## Zenon Docs
# QLDB Demo

1. Activate the virtual environment by running `source ./.env/bin/activate`
2. Run `python create_ledger.py` this creates a ledger which acts as a particular schema or collection of tables.

![ledge to relational](https://docs.aws.amazon.com/qldb/latest/developerguide/images/rdbms-mapping.png)

3. Run `python create_table.py` and `python create_index.py` this creates the tables and indexes required for the vehicle registration application.
4. Run `python insert_document.py` to populate the tables.
5. Run find queries `python find_vehicles.py`
6. Update a document by running `python transfer_vehicle_ownership.py`. This transfers the ownership from one user to another.
7. Update a document by running `python add_secondary_owner.py`. This adds a secondary owner to a vehicle.
8. You can query the history of a document by running `python query_history.py`.
9. You can efficiently verify the integrity of a document in your ledger's journal by using cryptographic hashing with SHA-256. Run `python get_revision.py`.

## License

This library is licensed under the MIT-0 License.
