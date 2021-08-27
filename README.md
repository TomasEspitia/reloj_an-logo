# reloj_an-logo

vertical_position = 0 

def setup (): 
    size (250, 500)
    background (215) 
    
def draw ():
    global vertical_position 
    background (215)
    fill (40, 125, 0)
    ellipse (width / 2, vertical_position, 50, 50)
    
    if vertical_position > height: 
        vertical_position = 0
    else: 
        vertical_position= map(second(), 0, 59, 0, height)
        
    fill (110, 255, 0)
    ellipse (width / 2, vertical_position, 50, 50)
    
    if vertical_position > height: 
        vertical_position = 0
    else: 
        vertical_position= map(minute(), 0, 59, 0, height)
        
    fill (105, 190, 0)
    ellipse (width / 2, vertical_position, 50, 50)
    
    if vertical_position > height: 
        vertical_position = 0
    else: 
        vertical_position= map(hour(), 0, 59, 0, height)
