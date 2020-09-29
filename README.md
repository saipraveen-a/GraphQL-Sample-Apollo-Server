# Apollo tutorial

This is the fullstack app for the [Apollo tutorial](http://apollographql.com/docs/tutorial/introduction.html). 🚀

## File structure

There are two folders (one for `server` and one for `client`).

## Installation

To run the app, run these commands in two separate terminal windows from the root:

```bash
cd server && npm i && npm start
```

and

```bash
cd client && npm i && npm start
```

## Corrections to Queries from tutorial

    query XYZ {
        launches {
            launches {
                mission {
                    name
                    missionPatch(size: LARGE)
                }
            }
        }
    }