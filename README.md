# CRUD API

A simple CRUD (Create, Read, Update, Delete) API built using Python.

## Installation

1. Clone the repository:
```
git clone https://github.com/your-username/crud-api.git
```

2. Navigate to the project directory:
```
cd crud-api
```

3. Create a virtual environment (optional but recommended):
```
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```

4. Install the required dependencies:
```
pip install -r requirements.txt
```

## Usage

1. Start the server:
```
python crud.py
```

2. The API will be available at `http://localhost:5000`.

## API

### Create
- **Endpoint**: `POST /items`
- **Request Body**: `{"name": "Item Name", "description": "Item Description"}`
- **Response**: `{"id": 1, "name": "Item Name", "description": "Item Description"}`

### Read
- **Endpoint**: `GET /items`
- **Response**: `[{"id": 1, "name": "Item Name", "description": "Item Description"}]`
- **Endpoint**: `GET /items/<int:item_id>`
- **Response**: `{"id": 1, "name": "Item Name", "description": "Item Description"}`

### Update
- **Endpoint**: `PUT /items/<int:item_id>`
- **Request Body**: `{"name": "Updated Name", "description": "Updated Description"}`
- **Response**: `{"id": 1, "name": "Updated Name", "description": "Updated Description"}`

### Delete
- **Endpoint**: `DELETE /items/<int:item_id>`
- **Response**: `{"message": "Item deleted"}`

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Create a new Pull Request

## License

This project is licensed under the [MIT License](LICENSE).

## Testing

To run the tests, execute the following command:
```
python -m unittest discover tests
```
