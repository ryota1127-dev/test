import sys
import pygame
from pygame.locals import QUIT

pygame.init()
SURFACE = pygame.display.set_mode((1200,700))
FPSCLOCK = pygame.time.Clock()

def main():
    sysfont = pygame.font.SysFont("Meiryo",100)
    message = sysfont.render("Hello World!",True,(0,255,255))
    message_rect = message.get_rect(center = (600,350))

    while True:
        for event in pygame.event.get():
            if event.type == QUIT:
                pygame.quit()
                sys.exit()
        SURFACE.fill((255,255,255))
        SURFACE.blit(message,message_rect)
        pygame.display.update()
        FPSCLOCK.tick(3)
if __name__ == '__main__':
    main()
