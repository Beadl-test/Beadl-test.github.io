---
layout: default
title: BEADL-XML example
parent:  BEADL XML
nav_order: 1
has_children: false
---
# BEADL-XML Example

For the following shown example of the implementation of the LightChasingTask, the corresponding BEADL-XML description is shown below.
![](../assets/images/BEADL_LightChasingTask_Diagram.PNG)

```xml
<?xml version="1.0" encoding="utf-8"?>
<BEADL version="0.1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="BEADL.xsd">
    <BeadlTrialProtocol name="LightChasingTask" startState="WaitForPoke" numberOfTrials="INF">
        <BeadlArguments>
            <BeadlArgument name="CorrectPortNum" expression="randi(3)" comment="random integer value in range [1..3] to define the port to be used as correct port" type="numeric" />
            <BeadlArgument name="RewardSize" expression="10" comment="reward size in microliter" type="numeric" />
            <BeadlArgument name="ValveTime" expression="GetValveTimes(RewardSize, ValveTime)" comment="convert the reward size into a duration the reward valve needs to be opened" type="numeric" />
            <BeadlArgument name="TimeOutDuration" expression="6" comment="Time out duration when the subject selected the wrong port" type="numeric" />
            <BeadlArgument name="ITIDuration" expression="6" comment="Inter-Trial-Interval" type="numeric" />
        </BeadlArguments>
        <HardwareSettings hardware="Bpod" version="r0.5">
            <ConnectionMapping name="CorrectPort" resourceName="port1" type="behavioralPort">
                <Dependency type="BeadlArgumentDependency" expression="CorrectPortNum == 1" />
            </ConnectionMapping>
            <ConnectionMapping name="CorrectPort" resourceName="port2" type="behavioralPort">
                <Dependency type="BeadlArgumentDependency" expression="CorrectPortNum == 2" />
            </ConnectionMapping>
            <ConnectionMapping name="CorrectPort" resourceName="port3" type="behavioralPort">
                <Dependency type="BeadlArgumentDependency" expression="CorrectPortNum == 3" />
            </ConnectionMapping>
            <ConnectionMapping name="ErrorPort1" resourceName="port2" type="behavioralPort">
                <Dependency type="BeadlArgumentDependency" expression="CorrectPortNum == 1" />
            </ConnectionMapping>
            <ConnectionMapping name="ErrorPort2" resourceName="port3" type="behavioralPort">
                <Dependency type="BeadlArgumentDependency" expression="CorrectPortNum == 1" />
            </ConnectionMapping>
            <ConnectionMapping name="ErrorPort1" resourceName="port1" type="behavioralPort">
                <Dependency type="BeadlArgumentDependency" expression="CorrectPortNum == 2" />
            </ConnectionMapping>
            <ConnectionMapping name="ErrorPort2" resourceName="port3" type="behavioralPort">
                <Dependency type="BeadlArgumentDependency" expression="CorrectPortNum == 2" />
            </ConnectionMapping>
            <ConnectionMapping name="ErrorPort1" resourceName="port1" type="behavioralPort">
                <Dependency type="BeadlArgumentDependency" expression="CorrectPortNum == 3" />
            </ConnectionMapping>
            <ConnectionMapping name="ErrorPort2" resourceName="port2" type="behavioralPort">
                <Dependency type="BeadlArgumentDependency" expression="CorrectPortNum == 3" />
            </ConnectionMapping>
        </HardwareSettings>
        <BeadlEvents>
            <HardwareEvent eventName="CorrectPortPoke" connection="CorrectPort.poke" type="" comment="" />
            <HardwareEvent eventName="ErrorPort1Poke" connection="ErrorPort1.poke" type="" comment="" />
            <HardwareEvent eventName="ErrorPort2Poke" connection="ErrorPort2.poke" type="" comment="" />
        </BeadlEvents>
        <BeadlActions>
            <HardwareAction actionName="CorrectPortLED" connection="CorrectPort.led" type="" comment="" />
            <HardwareAction actionName="CorrectPortValve" connection="CorrectPort.valve" type="" comment="" />
        </BeadlActions>
        <BeadlStates>
            <BeadlState name="WaitForPoke">
                <StateTimer>inf</StateTimer>
                <StateOutputActions>
                    <OutputAction actionName="CorrectPortLED" actionValue="on" />
                </StateOutputActions>
                <StateEvents>
                    <ExternalEvent eventName="CorrectPortPoke" eventValue="in" eventTransition="CorrectPortPoke_in" />
                    <ExternalEvent eventName="ErrorPort1Poke" eventValue="in" eventTransition="ErrorPort1Poke_in" />
                    <ExternalEvent eventName="ErrorPort2Poke" eventValue="in" eventTransition="ErrorPort2Poke_in" />
                </StateEvents>
                <Dependency type="BeadlArgumentDependency" expression="CorrectPortNum == 3" />
            </BeadlState>
            <BeadlState name="End">
                <StateTimer>inf</StateTimer>
                <StateOutputActions />
                <StateEvents />
            </BeadlState>
            <BeadlState name="Reward">
                <StateTimer>ValveTime</StateTimer>
                <StateOutputActions>
                    <OutputAction actionName="CorrectPortValve" actionValue="open" />
                </StateOutputActions>
                <StateEvents>
                    <TimerEvent eventName="stateExpired" eventValue="" eventTransition="stateExpired" timer="StateTimer" />
                </StateEvents>
            </BeadlState>
            <BeadlState name="ITI">
                <StateTimer>ITIDuration</StateTimer>
                <StateOutputActions />
                <StateEvents>
                    <TimerEvent eventName="stateExpired" eventValue="" eventTransition="stateExpired" timer="StateTimer" />
                </StateEvents>
            </BeadlState>
            <BeadlState name="TimeOut">
                <StateTimer>TimeOutDuration</StateTimer>
                <StateOutputActions />
                <StateEvents>
                    <TimerEvent eventName="stateExpired" eventValue="" eventTransition="stateExpired" timer="StateTimer" />
                </StateEvents>
            </BeadlState>
        </BeadlStates>
        <BeadlStateTransitions>
            <BeadlStateTransition from="Reward" to="ITI" eventTransition="stateExpired" label="" />
            <BeadlStateTransition from="WaitForPoke" to="Reward" eventTransition="CorrectPortPoke_in" label="" />
            <BeadlStateTransition from="WaitForPoke" to="TimeOut" eventTransition="ErrorPort1Poke_in" label="" />
            <BeadlStateTransition from="WaitForPoke" to="TimeOut" eventTransition="ErrorPort2Poke_in" label="" />
            <BeadlStateTransition from="TimeOut" to="ITI" eventTransition="stateExpired" label="" />
            <BeadlStateTransition from="ITI" to="End" eventTransition="stateExpired" label="" />
        </BeadlStateTransitions>
    </BeadlTrialProtocol>
</BEADL>
```

