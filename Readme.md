# Fresh Fruit
Aplikasi ini dapat digunakan oleh user dalam menambahkan maupun menghapus sebuah item yang berupa buah ke dalam keranjang.
# Scope & Functionailities
- User dapat menambahkan buah yang akan di pilih
- User dapat menghapus buah yang telah di pilih
- User akan mendapatkan sebuah notifikasi apabila keranjang telah penuh

## How Does it Works
Diawali method pada class `Bucket.cs` dengan mendeklarasikan :
```csharp
class Bucket
    {
        private int capacity;
        private List<Fruit> fruits;

        public Bucket(int capacity)
        {
            this.capacity = capacity;
            this.fruits = new List<Fruit>();
        }

        public void insert(Fruit fruit)
        {
            this.fruits.Add(fruit);
        }

        public void remove(int position)
        {
            this.fruits.RemoveAt(position);
        }

        public List<Fruit> findAll()
        {
            return this.fruits;
        }
        public int getCapacity()
        {
            return this.capacity;
        }
        public int countItems()
        {
            return this.fruits.Count();
        }
    }
```