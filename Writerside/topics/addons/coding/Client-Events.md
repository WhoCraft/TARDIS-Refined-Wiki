# Tardis Refined API Events (Client)

The TardisClientEvents class provides events for client-side functionality related to the TARDIS.

### Shell Entry Models Setup Event
#### SHELLENTRY_MODELS_SETUP
The SHELLENTRY_MODELS_SETUP event is triggered when setting up shell and interior models for the TARDIS. It provides the EntityModelSet context.

```java 
public interface SetupModels { 
    void setUpShellAndInteriorModels(EntityModelSet context);
} 
```


This event allows addon makers to register their custom shell and interior door models in a safe and controlled manner.

Note: This event is only triggered on the client-side, and is intended for use by addon makers who want to customize the appearance of the TARDIS.