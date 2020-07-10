# graphql-mesh-demo

Demo of GraphQL Mesh combining the Stripe REST API and the Github GraphQL API into one GraphQL endpoint.

## Run Demo

```bash
STRIPE_TOKEN=ADD_YOURS GH_ACCESS_TOKEN=ADD_YOURS yarn graphql-mesh serve
```

Then open http://localhost:4000/graphql

## Sample Query

```graphql
{
  STRIPE_getBalance {
    available {
      amount
    }
    livemode
    pending {
      amount
    }
  }
  STRIPE_getAccount {
    id
    email
  }
  GITHUB_user(login: "micmro") {
    name
  }
}
```
