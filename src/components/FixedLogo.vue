<template>
    <v-app id="inspire">
      <v-main>
        
        <v-container>
          <v-row>
            <v-col
            v-for="n in 2"
            :key="n"
            >
              <v-card height="300">
                <DashboardCard />
              </v-card>
              
            </v-col>
          </v-row>
        </v-container>
      </v-main>
    </v-app>
  </template>