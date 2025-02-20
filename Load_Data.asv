%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% ME-5339 Simulation Techniques for Dynamic Systems Analysis and Design
% M. Canova, Autumn 2020
%
% Course Project: Modeling and Control of Gas Turbine Dynamics
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
close all
clear all
clc

%% Problem Data:
load Compressor_Map.mat 
load Turbine_Map.mat
load Pow_demand.mat             % Load Grid Power Demand Data

J = 0.25;                       % Mass moment of inertia [kg*m^2]
pamb = 1e5;
Tamb = 298;
cp = 1200;
R = 310;
cv = cp-R;
gamma = cp/cv;                   % Specific heat ratio
lambda = (gamma-1)/gamma;
cp_m = 2300;                     % Specific heat methane [J/kg-K]
Q_LHV = 50e6;                    % Heating value [J/kg]

V = 2;                           % Combustion chamber volume [m^3]

mf = 0.035;
N0 = 90000;                      % Initial Speed [rpm]
p0 = 13e5;                        % Initial Pressure [Pa]
T0 = 1400;                       % Initial Temperature [K]
pl=200e3

m0= (p0*V)/(R*T0);
% 
% [sizes,x0,xstr] = Gas_Turbine_Model_2017a_mod([],[],[],0)
% 
% 
u0=[mf,pl]
x0=[p0,T0,N0];
% 
% 
[x,u,y,dx]= trim('Gas_Turbine_Model_2017a_mod',x0,u0)

% %% Plot compressor maps
% figure
% surf(N_cmp,Beta_cmp,Mf_cmp')
% xlabel('Shaft speed [rpm]')
% ylabel('Pressure ratio [-]')
% zlabel('Compressor flow rate [kg/s]')
% figure
% surf(N_cmp,Beta_cmp,Eta_cmp')
% xlabel('Shaft speed [rpm]')
% ylabel('Pressure ratio [-]')
% zlabel('Compressor efficiency [kg/s]')
% 
% %% Plot power consumption data from grid
% figure
% plot(time_data/3600,pow_data)
% hold on
% grid on
% xlabel('Time [hr]')
% ylabel('Grid power consumption [kW]')
% set(gca,'xlim',[0 24],'xtick',[0:3:24]);

