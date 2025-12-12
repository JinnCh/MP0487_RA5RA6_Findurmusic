```mermaid
classDiagram

    class Database {
        +getConnection() PDO
    }

    class UserController {
        - PDO conn

        + __construct()
        + login() void
        + logout() void
        + register() void
        + update() void
        + delete() void
    }

    class XController {
        - PDO conn

        + __construct()
        + create() void
        + update() void
        + delete() void
    }

    UserController --> Database : uses
    XController --> Database : uses
