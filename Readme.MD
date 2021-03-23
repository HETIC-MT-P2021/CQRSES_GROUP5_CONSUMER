![License](https://img.shields.io/github/license/HETIC-MT-P2021/CQRSES_GROUP5_CONSUMER)
![golang](https://img.shields.io/github/languages/top/HETIC-MT-P2021/CQRSES_GROUP5_CONSUMER)
![golang-version](https://img.shields.io/github/go-mod/go-version/HETIC-MT-P2021/CQRSES_GROUP5_CONSUMER)
![commit](https://img.shields.io/github/last-commit/HETIC-MT-P2021/CQRSES_GROUP5_CONSUMER)
![build-CI](https://img.shields.io/github/workflow/status/HETIC-MT-P2021/CQRSES_GROUP5_CONSUMER/CI)

# [GO CQRS ES Ordering Application](https://github.com/HETIC-MT-P2021/CQRSES_GROUP5) Consumer - Student Project

This consumer is linked with a [Go CQRS ES student project](https://github.com/HETIC-MT-P2021/CQRSES_GROUP5).

It receives messages from the main project Message Broker, and it writes into the Elastic Search database.

This project is built on a shared docker network with the main project.
## Usage

`git config core.hooksPath .githooks`

> Configure GitHooks

`cp docker-compose.yml.dist docker-compose.yml`

> Docker configuration override, don't forget to add the Token, SQL and RBMQ variables

` docker-compose up --build`

> Run the project

## License
[MIT](https://github.com/HETIC-MT-P2021/CQRSES_GROUP5_CONSUMER/blob/master/LICENSE.md)

## Main repository

[Main repository for this consumer](https://github.com/HETIC-MT-P2021/CQRSES_GROUP5)


## For further project documentation 

Please visit all the project documentation (functionnal and technical specs, architecture, etc.) in the [root doc of main project](https://github.com/HETIC-MT-P2021/CQRSES_GROUP5/blob/master/doc)

## Resources

### Order

| Field     | Type           | Editable | Description      |
| --------- | -------------- | -------- | ---------------- |
| id        | int            | no       | Order ID         |
| reference | string         | yes      | Order reference  |
| customer  | string         | yes      | Customer name    |
| time      | timestamp(UTC) | no       | Order created on |

### Order Lines

| Field    | Type            | Editable | Description              |
| -------- | --------------- | -------- | ------------------------ |
| id       | int             | no       | Order Line ID            |
| meal     | string          | yes      | Type of meal ordered     |
| quantity | int             | yes      | Quantity of meal ordered |
| price    | int             | no       | Meal price (single unit) |
| order_id | timestamp (UTC) | no       | Order ID                 |

### Generating a project documentation

`golds ./...`

> Start a local doc server

Or

`golds -gen -dir=generated -nouses ./...`

> Generate static HTML doc pages

`golds -dir=generated`

> View the generated doc

## Authors

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/Araknyfe">
        <img src="https://github.com/Araknyfe.png" width="150px;"/><br>
        <b>Athénaïs Dussordet</b>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/AlexandreLch">
        <img src="https://github.com/AlexandreLch.png" width="150px;"/><br>
        <b>Alexandre Lellouche</b>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/Traineau">
        <img src="https://github.com/Traineau.png" width="150px;"/><br>
        <b>Thomas Raineau</b>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/SteakBarbare">
        <img src="https://github.com/SteakBarbare.png" width="150px;"/><br>
        <b>Corto Dufour</b>
      </a>
    </td>
  </tr>
</table>
