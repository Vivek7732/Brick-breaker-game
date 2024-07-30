# Brick-breaker-game
		}
		repaint();
	}

	@Override
	public void keyPressed(KeyEvent e) {
		if (e.getKeyCode() == KeyEvent.VK_RIGHT) {
			if (playerX >= 583) {
				playerX = 583;
			} else {
				moveRight();
			}
		}

		if (e.getKeyCode() == KeyEvent.VK_LEFT) {
			if (playerX <= 3) {
				playerX = 3;
			} else {
				moveLeft();
			}
		}

		if (e.getKeyCode() == KeyEvent.VK_ENTER) {
			if (!play) {
				ballposX = 220;
				ballposY = 390;
				ballXDir = -1;
				ballYDir = -2;
				score = 0;
				playerX = 310;
				totalBricks = 21;
				map = new MapGenerator(3, 7);
				repaint();
			}
		}
	}

	@Override
	public void keyReleased(KeyEvent e) {
	}

	@Override
	public void keyTyped(KeyEvent e) {
	}

	public void moveRight() {
		play = true;
		playerX += 20;
	}

	public void moveLeft() {
		play = true;
		playerX -= 20;
	}

}
