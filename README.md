# Multithreading---distance-between-planets-aestroids
#include<stdio.h>
#include<pthread.h>
void*earth_mars(void*args) {
    printf("Distance between Earth and Mars = 225 million km\n");
    return NULL;}
void* earth_asteroid(void *arg) {
    printf("Distance between Earth and Asteroid = 54 million km\n");
    return NULL;}
int main() {
    pthread_t t1,t2;
    pthread_create(&t1 , NULL, earth_mars, NULL);
    pthread_create(&t2, NULL, earth_asteroid, NULL);
    pthread_join(t1, NULL);
    pthread_join(t2, NULL);
    printf("Distance calculations completed\n");
    return 0;}
  // output 
  Distance between Earth and Mars=225 million km
  Distance between Earth and astroid=54 million km
  Distance calculation completed.
  //
