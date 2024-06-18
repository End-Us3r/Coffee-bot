# Guided Python Project - Coffee Chatbot
## 10/23/2022

```python
def coffee_bot():
  print('Welcome to the cafe!')
  size = get_size()
  drink_type = get_drink_type()
  print('Alright, that\'s a ' + size + ' ' + drink_type + '!')
  name = input('Can I get your name please?\n')
  print('Thanks, ' + name + '! Your drink will be ready shortly.')

def print_message():
  print('I\'m sorry, I did not understand your selection. Please enter the corresponding letter for your response.')

def get_size():
  res = input('What size drink can I get for you? \n[a] Small \n[b] Medium \n[c] Large \n')
  if res == 'a':
    return 'Small'
  elif res == 'b':
    return 'Medium'
  elif res == 'c':
    return 'Large'
  else:
    print_message()
    return get_size()

def order_latte():
  res = input('And what kind of milk for your latte? \n[a] 2% Milk \n[b] Non-fat Milk \n[c] Soy Milk \n')
  if res == 'a':
    return 'Latte'
  elif res == 'b':
    return 'Non-fat Latte'
  elif res == 'c':
    return 'Soy Latte'
  else:
    print_message()
    return order_latte()

def get_drink_type():
  res = input('What type of drink would you like? \n[a] Brewed Coffee \n[b] Mocha \n[c] Latte \n')
  if res == 'a':
    return 'Brewed Coffee'
  elif res == 'b':
    return 'Mocha'
  elif res == 'c':
    return order_latte()
  else:
    print_message()
    return get_drink_type()

coffee_bot()
