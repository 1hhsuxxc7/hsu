#include <GL/glut.h>

void display()
{
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT);

    glColor3ub(158,154,248);/// unsigned byte是0...255
    glBegin(GL_TRIANGLES);

        glVertex2f((88-150)/150.0, -(11-150)/150.0);
        glVertex2f((149-150)/150.0,-(99-150)/150.0);
        glVertex2f((140-150)/150.0,-(56-150)/150.0);

    glEnd();


    glutSwapBuffers();
}
int main(int argc, char ** argv)
{
    glutInit(&argc, argv);
    glutInitDisplayMode(GLUT_DOUBLE | GLUT_DEPTH);
    glutCreateWindow("08160600");

    glutDisplayFunc(display);

    glutMainLoop();

}
