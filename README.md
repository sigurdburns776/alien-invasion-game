import sys

import pygame

from game_settings import Settings

def run_game():
    #Initialize game and create a screen object
    pygame.init()
    ai_settings = Settings()
    screen = pygame.display.set_mode((ai_settings.screen_width, ai_settings.screen_height))
    screen = pygame.display.set_mode((1200,800))
    pygame.display.set_caption("Alien Invasion")
    
    #setting the background screen color
    bg_color = (230 , 230, 230)
    

    #start main loop for the game
    while True:
        #Watch for keyboard and mouse events
        for event in pygame.event.get():
            if event.type == pygame.QUIT:
                sys.exit
                
        #redraw the screen during each pass through the loop. 
        screen.fill(ai_settings.bg_color)
        
        #Make the most recently drawns screen visible
        
        pygame.display.flip()

run_game()
    
