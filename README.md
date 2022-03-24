# GraphQLRestarauntData
Coding assignment in MIT XPro Fullstack program uing graphql
To Run: npm install express express-graphql graphql then run node server with this code: node index.js

Below is the code for the graphql results:

mutation editrestaurants($idd: Int = 1, $name: String = "OLDO") {
  editrestaurant(id: $idd, name: $name) {
    name
    description
  }
}

mutation setrestaurants {
  setrestaurant(input: {
    name: "Granite",
    description: "American",
  }) {
    name
    description
  }
}

mutation deleterestaurants($iid: Int = 1) {
  deleterestaurant(id: $iid) {
    ok
  }
}

query getrestaurants {
  restaurants {
    name
    description
    dishes {
      name
      price
    }
  }
}
query getrestaurant($iid: Int = 1) {
        restaurant(id: $iid) {
    name
    description
  }
}
