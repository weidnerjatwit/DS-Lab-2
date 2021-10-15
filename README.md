# DS-Lab-2
import pygame
 
# define a main function
def main():
     
    # initialize the pygame module

    pygame.init()

    pygame.display.set_caption("Lab 2")
    screen = pygame.display.set_mode((800,400))
    WIDTH = 800
    HEIGHT = 400
    pygame.display.update()
    # load and set the logo
    #logo = pygame.image.load("logo32x32.png")
    # pygame.display.set_icon(logo)
    # pygame.display.set_caption("minimal program")
    wcolor = pygame.Color("blue")
    Border = 20
    pygame.draw.rect(screen, wcolor, pygame.Rect((0,0),(WIDTH,Border)))
    Thick = 20
    pygame.draw.rect(screen, wcolor, pygame.Rect((0,0),(Thick,HEIGHT)))
    
    pygame.draw.rect(screen, wcolor, pygame.Rect((0,380),(WIDTH,Border)))
    
    pygame.display.update()


    # create a surface on screen that has the size of 240 x 180
    #screen = pygame.display.set_mode((240,180))
     
    # define a variable to control the main loop
    running = True
     
    # main loop
    while running:
        # event handling, gets all event from the event queue
        for event in pygame.event.get():
            # only do something if the event is of type QUIT
            if event.type == pygame.QUIT:
                # change the value to False, to exit the main loop
                running = False
     
     
# run the main function only if this module is executed as the main script
# (if you import this as a module then nothing is executed)
if __name__=="__main__":
    # call the main function
    main()
