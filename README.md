# Ивана Велинова 223200
# 2.![Control Flow Graph](Untitled Diagram.drawio (1).png)
# 3.Цикломатската комплексност 
Цикломатската комплексност на овој код е 10, истата ја добив преку формулата P+1, каде што P е бројот на предикатни јазли. Во случајoв P=9, па цикломатската комплексност изнесува 10.
# Tест случаи според Every Branch критериумот
 1.allItems=null,payment=100
- Кога имаме празна листа,враќа allItems list can't be null!
2.allItems = [], payment = 100
- Враќа true (бидејќи збирот е 0, што е помало или еднакво на уплатата)
3.allItems = [new Item(null, "123456", 100, 0)], payment = 100
- Враќа true(името на ставката е поставено на „unknown“)
4.allItems = [new Item("", "123456", 100, 0)], payment = 100
- Враќа true(името на ставката е поставено на „unknown“)
5.allItems = [new Item("item1", null, 100, 0)], payment = 100
- Баркодот е null.Враќа No barcode!
6.allItems = [new Item("item1", "12345a", 100, 0)], payment = 100
- Баркодот содржи неважечки знак(буква).Враќа Invalid character in item barcode!
7.allItems = [new Item("item1", "123456", 100, 0.1f)], payment = 90
- Враќа true (Цената со попуст е 100 * 0.1 = 10, вкупната сума е 10)
8.allItems = [new Item("item1", "0123456", 350, 0.2f)], payment = 30
- Враќа true (цената со попуст е 350 * 0,2 = 70, се применува -30 попуст, вкупната сума е 40)
9.allItems = [new Item("item1", "123456", 100, 0), new Item("item2", "789012", 200, 0.1f)], payment = 270
- Враќа true (збирот е 100 + 20 = 120, што е помало од плаќањето)
10.allItems = [new Item("item1", "123456", 100, 0), new Item("item2", "789012", 200, 0.1f)], payment = 100
- Враќа false (збирот е 100 + 20 = 120, што е повеќе од плаќањето)



