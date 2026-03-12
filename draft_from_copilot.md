classDiagram
    class Customer {
        +name: String
        +purchaseHistory: List~Order~
        +verifyUser(): boolean
    }
    
    class FoodItem {
        +name: String
        +price: double
        +category: String
        +popularityRating: int
    }
    
    class Menu {
        +items: List~FoodItem~
        +filterByCategory(category: String): List~FoodItem~
    }
    
    class Order {
        +items: List~FoodItem~
        +totalCost: double
        +computeTotalCost(): double
    }
    
    Customer --> Order : has
    Menu --> FoodItem : contains
    Order --> FoodItem : contains