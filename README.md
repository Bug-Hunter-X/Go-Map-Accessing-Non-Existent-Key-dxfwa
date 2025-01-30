# Go Map Accessing Non-Existent Key

This example demonstrates a common issue in Go: accessing a non-existent key in a map.

In many languages, accessing a non-existent key in a map would throw an exception or cause a runtime error. However, Go handles this differently.  Instead of panicking, it returns the zero value for the map's value type.  This can lead to unexpected behavior if not handled carefully.

**Example:**
The `bug.go` file shows how accessing a missing key in a map returns 0 (the zero value for `int`). This might not be immediately apparent and could introduce subtle bugs in your application.

**Solution:**
The `bugSolution.go` file provides a more robust approach. It uses the comma ok idiom to explicitly check if the key exists before accessing the value.

This approach avoids potential runtime errors and makes the code's intent clearer.