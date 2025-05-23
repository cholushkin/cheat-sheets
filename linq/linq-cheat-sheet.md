| Filtering     | Description                            | Example                                       |
| ------------- | -------------------------------------- | --------------------------------------------- |
| **Where**     | Filters elements                       | `var result = numbers.Where(n => n > 3);`     |
| **Distinct**  | Removes duplicate elements             | `var distinct = numbers.Distinct();`          |
| **Take**      | Takes the first N elements             | `var firstThree = numbers.Take(3);`           |
| **TakeWhile** | Takes elements while condition is true | `var result = numbers.TakeWhile(n => n < 4);` |
| **Skip**      | Skips the first N elements             | `var skipFirstThree = numbers.Skip(3);`       |
| **SkipWhile** | Skips elements while condition is true | `var result = numbers.SkipWhile(n => n < 4);` |

-----

| Projection (Transforming Data) | Description                         | Example                                               |
| ------------------------------ | ----------------------------------- | ----------------------------------------------------- |
| **Select**                     | Projects elements                   | `var squared = numbers.Select(n => n * n);`           |
| **SelectMany**                 | Flattens a sequence of sequences    | `var flat = lists.SelectMany(l => l);`                |
| **Zip**                        | Combines two sequences element-wise | `var zipped = numbers.Zip(letters, (n, l) => n + l);` |

-----

| Sorting            | Description                           | Example |
|-------------------|--------------------------------------|---------|
| **OrderBy**      | Sorts in ascending order            | `var ordered = numbers.OrderBy(n => n);` |
| **OrderByDescending** | Sorts in descending order      | `var orderedDesc = numbers.OrderByDescending(n => n);` |
| **ThenBy**       | Secondary sorting in ascending order | `var sorted = numbers.OrderBy(n => n).ThenBy(n => n % 2);` |
| **ThenByDescending** | Secondary sorting in descending order | `var sorted = numbers.OrderBy(n => n).ThenByDescending(n => n % 2);` |
| **Reverse**      | Reverses sequence order             | `var reversed = numbers.Reverse();` |

-----

| Grouping and Joining | Description                           | Example |
|----------------------|--------------------------------------|---------|
| **GroupBy**        | Groups elements by a key            | `var grouped = numbers.GroupBy(n => n % 2 == 0);` |
| **Join**           | Joins two sequences on a key        | `var joined = students.Join(courses, s => s.CourseId, c => c.CourseId, (s, c) => new { s.Name, c.CourseName });` |
| **GroupJoin**      | Groups matching elements from both sequences | `var groupJoined = students.GroupJoin(courses, s => s.CourseId, c => c.CourseId, (s, cs) => new { s.Name, Courses = cs });` |

-----

| Set Operations     | Description                           | Example |
|--------------------|--------------------------------------|---------|
| **Union**        | Combines two sequences, removing duplicates | `var unique = numbers.Union(new List<int> { 4, 5 });` |
| **Intersect**    | Returns common elements              | `var common = numbers.Intersect(new List<int> { 3, 4 });` |
| **Except**       | Removes elements from another sequence | `var difference = numbers.Except(new List<int> { 1, 2 });` |
| **Concat**       | Concatenates two sequences          | `var combined = numbers.Concat(new List<int> { 6, 7 });` |

-----

| Quantifiers (Checking Conditions) | Description                           | Example |
|-----------------------------------|--------------------------------------|---------|
| **Any**           | Checks if any element matches a condition | `bool hasEven = numbers.Any(n => n % 2 == 0);` |
| **All**           | Checks if all elements match a condition | `bool allEven = numbers.All(n => n % 2 == 0);` |
| **Contains**      | Checks if a sequence contains a value | `bool hasThree = numbers.Contains(3);` |

-----

| Element Selection  | Description                           | Example |
|--------------------|--------------------------------------|---------|
| **First**        | Gets the first element               | `var firstEven = numbers.First(n => n % 2 == 0);` |
| **FirstOrDefault** | Gets first element or default      | `var firstEven = numbers.FirstOrDefault(n => n % 2 == 0);` |
| **Last**         | Gets the last element               | `var lastEven = numbers.Last(n => n % 2 == 0);` |
| **LastOrDefault** | Gets last element or default       | `var lastEven = numbers.LastOrDefault(n => n % 2 == 0);` |
| **Single**       | Gets a single element or throws if multiple found | `var single = numbers.Single(n => n == 3);` |
| **SingleOrDefault** | Gets a single element or default if none found | `var single = numbers.SingleOrDefault(n => n == 10);` |
| **ElementAt**    | Retrieves an element at an index    | `var item = numbers.ElementAt(2);` |
| **ElementAtOrDefault** | Retrieves an element or default if index is out of range | `var item = numbers.ElementAtOrDefault(10);` |

-----

| Aggregation   | Description                        | Example                                         |
| ------------- | ---------------------------------- | ----------------------------------------------- |
| **Count**     | Counts elements matching condition | `var count = numbers.Count(n => n % 2 == 0);`   |
| **Sum**       | Sums up elements                   | `var sum = numbers.Sum();`                      |
| **Min**       | Gets the minimum value             | `var min = numbers.Min();`                      |
| **Max**       | Gets the maximum value             | `var max = numbers.Max();`                      |
| **Average**   | Calculates the average             | `var average = numbers.Average();`              |
| **Aggregate** | Applies a function over a sequence | `var sum = numbers.Aggregate((a, b) => a + b);` |

-----

| Conversion        | Description                           | Example |
|-------------------|--------------------------------------|---------|
| **ToList**       | Converts to a list                  | `var list = numbers.ToList();` |
| **ToArray**      | Converts to an array                | `var array = numbers.ToArray();` |
| **ToDictionary** | Converts to a dictionary           | `var dict = numbers.ToDictionary(n => n, n => n * n);` |
| **Cast**         | Casts elements to a type            | `var casted = objects.Cast<int>();` |
| **OfType**       | Filters elements by type           | `var ints = objects.OfType<int>();` |

-----

| Execution Types  | Description                           | Example |
|-----------------|--------------------------------------|---------|
| **Deferred Execution** | Queries execute when iterated | `var query = numbers.Where(n => n > 3);` |
| **Immediate Execution** | Executes immediately         | `var list = query.ToList();` |

-----

| Anonymous Types  | Description                           | Example |
|-----------------|--------------------------------------|---------|
| **Anonymous Types** | Creates new type structures | `var result = students.Select(s => new { s.Name, s.Age });` |

ver.1.0
#prj-cheat-sheets #LINQ 
