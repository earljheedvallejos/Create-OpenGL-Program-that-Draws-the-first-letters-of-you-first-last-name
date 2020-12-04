# Create-OpenGL-Program-that-Draws-the-first-letters-of-you-first-last-name



#include <GL/glut.h>
		
		void display();
		void reshape(int,int);
		void timer(int);
		
		void init()
		{
		glClearColor(0.0f, 0.0f, 0.0f, 0.0f);
		glEnable(GL_DEPTH_TEST);
		
		}
		
		int main(int argc,char**argv)
		{
		glutInit(&argc,argv);
		glutInitDisplayMode(GLUT_RGB | GLUT_DOUBLE | GLUT_DEPTH);
		glutInitDisplayMode(GLUT_RGB);
		
		glutInitWindowPosition(0,0);
		glutInitWindowSize(700,600);
		glutCreateWindow("EARL VALLEJOS BS EMC DAT2A ");
		
		glutDisplayFunc(display);
		glutReshapeFunc(reshape);
		glutTimerFunc(0,timer,0);
		init();
		
		glutMainLoop();
		}
			
		void display()
		{
		
		glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT);
		glLoadIdentity();	
		glTranslatef(0.0f,0.0f,-8.0);
		glBegin(GL_QUADS);
	
		//E Base!
	glColor3f(0.0,0.0,1.0);
	glVertex2f(-7,1);
	glVertex2f(-10,-10);
	glVertex2f(-8,-10);
	glVertex2f(-5,1);
	
		//E Upper hLine!
	glColor3f(0.0,0.0,1.0);
	glVertex2f(-4.5,1);
	glVertex2f(-5,-1);
	glVertex2f(0,-1);
	glVertex2f(0.5,1);

		//E middle hLine!
	glColor3f(0.0,0.0,1.0);
	glVertex2f(-5.70,-3.5);
	glVertex2f(-6.25,-5.5);
	glVertex2f(-1.5,-5.5);
	glVertex2f(-1,-3.5);
	
		//E lower hLine!
	glColor3f(0.0,0.0,1.0);
	glVertex2f(-7,-8);
	glVertex2f(-7.50,-10);
	glVertex2f(-2.5,-10);
	glVertex2f(-2,-8);

		//VS Lline!
	glColor3f(0.0,0.0,1.0);
	glVertex2f(3,1);
	glVertex2f(6.75,-9.75);
	glVertex2f(7.75,-6.75);
	glVertex2f(5,1);

		//VS Rline!
	glColor3f(0.0,0.0,1.0);
	glVertex2f(11,1);
	glVertex2f(7,-10);
	glVertex2f(9,-10);
	glVertex2f(13,1);

	glEnd();
	glutSwapBuffers();
}
		
		void reshape(int w, int h)
		{
		glViewport(0,0, (GLsizei)w, (GLsizei)h);
		glMatrixMode(GL_PROJECTION);
		glLoadIdentity();
		gluPerspective(150,1,2.0,100.0);
		glMatrixMode(GL_MODELVIEW);
		
		}
		
		void timer(int)
		{
		glutPostRedisplay();
		glutTimerFunc(1000/60,timer,0);
		//Programmed by: EARL VALLEJOS BSEMCDAT2
		}
