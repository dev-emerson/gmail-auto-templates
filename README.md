# gmail-auto-templates
# Simple codes for sending emails with python and don't have to manually send templates to customers in a 1920x1080 monitor, but general 
# Running code through JupyterNotebook 


import pyautogui as pg
import pyperclip as pc

pg.PAUSE = 1.4 

emails = ['silva.ex@gmail.com', 	
'fortaleza.ex@gmail.com',	
'teixeira.ex@gmail.com',	
'coordenacao.ex@gmail.com',	
'operacoes.ex@gmail.com',	
'natalia.ex@gmail.com']


for customer in emails: 

    pg.hotkey('ctrl','2')
    pg.click(x=144, y=196)  # Write
    pg.click(x=1254, y=362) # Destiny 

    pc.copy(customer)
    pg.hotkey('ctrl','v')

    pg.click(x=1626, y=994) # 3 dots
    pg.click(x=1721, y=746) # Templates
    pg.click(x=1437, y=421) # Subject
    pg.click(x=1372, y=995) # Attachment
    pg.click(x=1351, y=740) # Attach button
    pg.click(x=115, y=190) # Desktop folder
    pg.click(x=324, y=208) # File
    pg.click(x=755, y=562) # Open
    pg.hotkey('del') # gmail gives me a little unwanted space between the template and my mail signature. 

    pg.click(x=1232, y=993) # Send 
    
#To get the position of the mouse if you need to adjust anything

import time

time.sleep(5)
pg.position()
