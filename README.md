# Game Over ke andar replace karo
show_text("💥 Game Over!", 50, RED, WIDTH//4, HEIGHT//2 - 50)
show_text(f"Your Score: {score}", 40, BLACK, WIDTH//4, HEIGHT//2 + 10)
show_text("Press R to Restart", 30, BLUE, WIDTH//4, HEIGHT//2 + 60)
pygame.display.update()

waiting = True
while waiting:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            pygame.quit()
            sys.exit()
        if event.type == pygame.KEYDOWN:
            if event.key == pygame.K_r:  # restart
                enemies.clear()
                bullets.clear()
                score = 0
                player_x = WIDTH // 2 - player_width // 2
                waiting = False
