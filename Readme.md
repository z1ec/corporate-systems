# corporate-systems
### My project for university, third semester, subject: corporate systems
---
The file 'Program.cs' contains the solution of 1 practical workbook.  

#### Implemented limitations for the calculator:
- dividing by 0
  implemented a restriction for division by 0 operations
  ```csharp
    case "/":
      if (num2 == 0)
      {
          throw new DivideByZeroException("Error: Division by zero is not allowed!");
      }
      result = num1 / num2;
      break;
  ```

- maximum of 5 decimal places
    ```csharp
    if (input.Contains('.'))
                {
                    string[] parts = input.Split('.');
                    if (parts.Length > 1 && parts[1].Length > 5)
                    {
                        Console.WriteLine("Warning: More than 5 decimal places detected. Truncating to 5 decimal places.");
                        input = parts[0] + "." + parts[1].Substring(0, 5);
                    }
                }
    ```

- the output value is between -10_000_000 and 10_000_000
    ```csharp
    if (result < -10000000 || result > 10000000)
                        {
                            throw new OverflowException($"Error: Result {result} is out of range (-10,000,000 to 10,000,000)!");
                        }
    ```
