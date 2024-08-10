# Tardis Refined API Events (Common)

The Tardis Refined API provides several events that allow developers to interact with the TARDIS's functionality. These events are triggered at specific points in the TARDIS's lifecycle, such as when it takes off, lands, or changes its shell.

### Take Off Event
#### `TAKE_OFF`
The `TAKE_OFF` event is triggered when a TARDIS takes off. It provides the `TardisLevelOperator`, `LevelAccessor`, and `BlockPos` of the TARDIS.

```java
public interface TakeOff {
    EventResult onTakeOff(TardisLevelOperator tardisLevelOperator, LevelAccessor level, BlockPos pos);
}
```

### Land Event
#### `LAND`
The `LAND` event is triggered when a TARDIS lands. It provides the `TardisLevelOperator`, `LevelAccessor`, and `BlockPos` of the TARDIS.

```java
public interface Land {
    void onLand(TardisLevelOperator tardisLevelOperator, LevelAccessor level, BlockPos pos);
}
```

### TARDIS Entry Event
#### `TARDIS_ENTRY_EVENT` {id="tardis-entry-event_1"}
The `TARDIS_ENTRY_EVENT` is triggered when a living entity enters a TARDIS. It provides the `TardisLevelOperator`, `LivingEntity`, `TardisNavLocation` of the source, and `TardisNavLocation` of the destination.

```java
public interface TardisEntry {
    void onEnterTardis(TardisLevelOperator tardisLevelOperator, LivingEntity livingEntity, TardisNavLocation sourceLocation, TardisNavLocation destinationLocation);
}
```

### TARDIS Exit Event
#### `TARDIS_EXIT_EVENT` {id="tardis-exit-event_1"}
The `TARDIS_EXIT_EVENT` is triggered when a living entity exits a TARDIS. It provides the `TardisLevelOperator`, `LivingEntity`, `TardisNavLocation` of the source, and `TardisNavLocation` of the destination.

```java
public interface TardisExit {
    void onExitTardis(TardisLevelOperator tardisLevelOperator, LivingEntity livingEntity, TardisNavLocation sourceLocation, TardisNavLocation destinationLocation);
}
```

### Door Closed Event
#### `DOOR_CLOSED_EVENT` {id="door-closed-event_1"}
The `DOOR_CLOSED_EVENT` is triggered when the TARDIS door is closed. It provides the `TardisLevelOperator`.

```java
public interface CloseDoor {
    void onDoorClosed(TardisLevelOperator tardisLevelOperator);
}
```

### Door Opened Event
#### `DOOR_OPENED_EVENT` {id="door-opened-event_1"}
The `DOOR_OPENED_EVENT` is triggered when the TARDIS door is opened. It provides the `TardisLevelOperator`.

```java
public interface OpenDoor {
    void onDoorOpen(TardisLevelOperator tardisLevelOperator);
}
```

### Shell Change Event
#### `SHELL_CHANGE_EVENT` {id="shell-change-event_1"}
The `SHELL_CHANGE_EVENT` is triggered when the TARDIS changes its shell. It provides the `TardisLevelOperator`, `ResourceLocation` of the theme, and a boolean indicating if the shell change was caused by a TARDIS being set up from a root shell.

```java
public interface ShellChange {
    void onShellChange(TardisLevelOperator tardisLevelOperator, ResourceLocation theme, boolean isSetupTardis);
}
```

### Desktop Change Event
#### `DESKTOP_CHANGE_EVENT` {id="desktop-change-event_1"}
The `DESKTOP_CHANGE_EVENT` is triggered when the TARDIS desktop is changed. It provides the `TardisLevelOperator`.

```java
public interface DesktopChangeEvent {
    void onDesktopChange(TardisLevelOperator tardisLevelOperator);
}
```

### TARDIS Crash Event
#### `TARDIS_CRASH_EVENT` {id="tardis-crash-event_1"}
The `TARDIS_CRASH_EVENT` is triggered when a TARDIS crashes. It provides the `TardisLevelOperator` and `TardisNavLocation` of the crash.

```java
public interface TardisCrash {
    void onTardisCrash(TardisLevelOperator tardisLevelOperator, TardisNavLocation crashLocation);
}
```

### Upgrade Unlocked Event
#### `UPGRADE_UNLOCKED`
The `UPGRADE_UNLOCKED` event is triggered when a TARDIS unlocks a new upgrade. It provides the `TardisLevelOperator` and `Upgrade`.

```java
public interface UpgradeUnlocked {
    void onUpgradeUnlock(TardisLevelOperator tardisLevelOperator, Upgrade upgrade);
}
```

### Player Control Interact Event
#### `PLAYER_CONTROL_INTERACT`
The `PLAYER_CONTROL_INTERACT` event is triggered when checking if player control can be used. It provides the `TardisLevelOperator`, `Control`, and `ControlEntity`.

```java
public interface CanControlBeUsed {
    EventResult canControlBeUsed(TardisLevelOperator tardisLevelOperator, Control control, ControlEntity controlEntity);
}
```

### TARDIS Setup Event
#### `TARDIS_SETUP_EVENT` {id="tardis-setup-event_1"}
The `TARDIS_SETUP_EVENT` is triggered when a TARDIS is set up from a root shell. It provides the `TardisLevelOperator`.

```java
public interface TardisSetup {
    void onTardisSetup(TardisLevelOperator tardisLevelOperator);
}
```

### TARDIS Break Event
#### `TARDIS_BREAK_EVENT` {id="tardis-break-event_1"}
The `TARDIS_BREAK_EVENT` is triggered when a TARDIS breaks. It provides the `TardisLevelOperator` and `TardisNavLocation` of the break.

```java
public interface TardisBreak {
    void onTardisBreak(TardisLevelOperator tardisLevelOperator, TardisNavLocation breakLocation);
}
```

### TARDIS Repair Event
#### `TARDIS_REPAIR_EVENT` {id="tardis-repair-event_1"}
The `TARDIS_REPAIR_EVENT` is triggered when a TARDIS is repaired. It provides the `TardisLevelOperator` and `TardisNavLocation` of the repair.

```java
public interface TardisRepair {
    void onTardisRepair(TardisLevelOperator tardisLevelOperator, TardisNavLocation repairLocation);
}
```

### TARDIS Dematerialize Event
#### `TARDIS_DEMATERIALIZE_EVENT` {id="tardis-dematerialize-event_1"}
The `TARDIS_DEMATERIALIZE_EVENT` is triggered when a TARDIS dematerializes. It provides the `TardisLevelOperator`.

```java
public interface TardisDematerialize {
    void onTardisDematerialize(TardisLevelOperator tardisLevelOperator);
}
```

### TARDIS Rematerialize Event
#### `TARDIS_REMATERIALIZE_EVENT` {id="tardis-rematerialize-event_1"}
The `TARDIS_REMATERIALIZE_EVENT` is triggered when a TARDIS rematerializes. It provides the `TardisLevelOperator`.

```java
public interface TardisRematerialize {
    void onTardisRematerialize(TardisLevelOperator tardisLevelOperator);
}
```