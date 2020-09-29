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

## Sample Queries and Mutations

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

    query loggedInUser {
        me {
            email
            id
            profileImage
	    }
    }

    mutation logIn {
        login(email : "saipraveen.a.iiit@gmail.com") {
            email
            id
        }
    }

    query GetLaunches {
        launches(pageSize: 10) {
            cursor
            hasMore
            launches {
                mission {
                    name
                }
            }
        }
    }

    query GetLaunchById($id: ID!) {
        launch(id: $id) {
            id
            rocket {
                id
                type
            }
        }
    }