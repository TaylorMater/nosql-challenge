Riley Taylor

UTA Data Analytics Bootcamp

Module 12 - NoSQL, mongodb, and pymongo




## Description

This contains my submission for module 12 of the UTA Data Analytics Bootcamp. We were tasked with completing two supplied jupyter notebooks that would test the use of mongodb and pymongo.


## Requirements

First, you need something to handle the jupyter notebooks (after installing jupyter notebook from conda/pip into your environment) - VSCode has extensions for this, and you can run `jupyter notebook` from the command line to make changes to notebooks in the browser. 

To be able to run the jupyter notebooks, you will need the following libraries (explicit versions given, but most should be valid):


-   Libraries: 
    - pymongo (v 4.6.2)
    - pandas (v 2.1.4)
-   Tools:
    - mongod.exe (v 7.0.6)
    - mongosh.exe (v 2.1.5)   
    - mongoimport.exe (v 100.9.4 )

The project was run using Python 3.10.13. 

Also, for future reference, a useful way to check your library version in a dev environment if the normal --version isn't working:

```
python -c 'import <library>; print (<library>.__version__)'
```

Thanks to [here](https://stackoverflow.com/questions/32221694/how-to-know-which-version-of-pymongo-is-running-on-my-project) for this command.

## Installation

Install by cloning the repo and using the tool of your choice to handle the jupyter notebooks. 

## Repo Overview 

`Resources/` contains the `establishments.json` file, which is used to import into the database. See the `NoSQL_setup.ipynb` to see the import command.

`NoSQL_analysis.ipynb` is the jupyter notebook that focused on answering questions/creating specific queries for the database.

`NoSQL_setup.ipynb` is the jupyter notebook that sets up the `'uk_food'` database so we could do analysis, and handled the import from the `.json` file in the `Resources/` directory. 

## Notes


My Tutor advised to not use the `Decimal` type, but instead to use `Double` type. It's less precise, but considering the accuracy we are working with is in the order of 0.01, it's not very relevant. For IEEE-754 double, it guarantees 15 digits (base 10) to be accurate in scientific notation, which is more than sufficient for our cases, see [here](https://stackoverflow.com/questions/28045787/how-many-decimal-places-does-the-primitive-float-and-double-support) 


-----------------------------

## Sources 
### Note - many of these were used for knowledge acquisition, with no direct reference to their content in this assignment. 



mongodb - how to get list of all databases in a mongo instance using pymongo - Stack Overflow
https://stackoverflow.com/questions/43501503/how-to-get-list-of-all-databases-in-a-mongo-instance-using-pymongo

collection – Collection level operations - PyMongo 4.6.2 documentation
https://pymongo.readthedocs.io/en/stable/api/pymongo/collection.html#pymongo.collection.Collection.drop

collection – Collection level operations - PyMongo 4.6.2 documentation
https://pymongo.readthedocs.io/en/stable/api/pymongo/collection.html#pymongo.collection.Collection.delete_many

mongodb - How to change the type of a field? - Stack Overflow
https://stackoverflow.com/questions/4973095/how-to-change-the-type-of-a-field

$toDecimal (aggregation) — MongoDB Manual
https://www.mongodb.com/docs/manual/reference/operator/aggregation/toDecimal/

python - MongoDB NumberDecimal: unsupported operand type(s) for +: 'Decimal128' and 'Decimal128' - Stack Overflow
https://stackoverflow.com/questions/41308044/mongodb-numberdecimal-unsupported-operand-types-for-decimal128-and-deci
