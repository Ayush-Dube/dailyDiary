### ⚡feb2

- tuple unpacking   
    - tuple is immutable , can be confusing in crud also can not be changed 
    - therefore json is used ,it takes dictionaries well , readlable and mutable over tuples.

           👉
            data = (400000, 0.05)  # Tuple with two values
             slab, rate = data  # Unpacking the tuple into two variables

            print(slab)  # Output: 400000
            print(rate)  # Output: 0.05

           👉
            tax_slabs = [
            (400000, 0.05),
            (800000, 0.10),
            (1200000, 0.15)
            ]

            for slab, rate in tax_slabs:
                print(f"Slab: {slab}, Rate: {rate}")




- Dictionaries Are More Suitable for Databases & APIs  

      -JSON (used in APIs & databases) is based on key-value pairs (similar to dictionaries). 

- tuple example

        def create_player(name, game, age, height, weight):
        return (name, game, age, height, weight)  # Returns a tuple

        # Example usage
        player = create_player("Leo", "Football", 35, 1.75, 72)

        # Unpacking the tuple
        name, game, age, height, weight = player

        print(f"Player: {name}, Sport: {game}, Age: {age}, Height: {height}m, Weight: {weight}kg")   

- 
