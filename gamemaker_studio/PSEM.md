# Particle System Emitter (PSEM) list item types

All member types are 4 bytes in size

GMS 2023.2.1.75 (adapted from original UndertaleParticleSystem.cs)
```
struct Emitter_2023_2 {
    string_offset Name;
    int Mode;
    int EmitCount, Distribution, Shape;
    float RegionX, RegionY, RegionWidth, RegionHeight, Rotation;
    sprite_offset sprite;
    int Texture;
    float FrameIndex;
    uint StartColor, MidColor, EndColor;
    bool AdditiveBlend;
    float LifetimeMin, LifetimeMax,
        ScaleX, ScaleY, SizeMin, SizeMax, SizeIncrease, SizeWiggle,
        SpeedMin, SpeedMax, SpeedIncrease, SpeedWiggle,
        GravityForce, GravityDirection,
        DirectionMin, DirectionMax, DirectionIncrease, DirectionWiggle,
        OrientationMin, OrientationMax, OrientationIncrease, OrientationWiggle;
    bool OrientationRelative;
    emitter_offset spawnOnDeath;
    int SpawnOnDeathCount;
    emitter_offset spawnOnUpdate;
    int SpawnOnUpdateCount;
};
```

GMS 2023.4.0.84
```
struct Emitter_2023_4 {
    string_offset Name;
    int Mode, EmitCount, Distribution, Shape;
    float RegionX, RegionY, RegionWidth, RegionHeight, Rotation;
    sprite_offset sprite;
    int Texture;
    float FrameIndex;
    
    bool Animate, Stretch, Random;  // New in 2023.4
    
    uint StartColor, MidColor, EndColor;
    bool AdditiveBlend;
    float LifetimeMin, LifetimeMax,
        ScaleX, ScaleY, SizeMin, SizeMax, SizeIncrease, SizeWiggle,
        SpeedMin, SpeedMax, SpeedIncrease, SpeedWiggle,
        GravityForce, GravityDirection,
        DirectionMin, DirectionMax, DirectionIncrease, DirectionWiggle,
        OrientationMin, OrientationMax, OrientationIncrease, OrientationWiggle;
    bool OrientationRelative;
    emitter_offset spawnOnDeath;
    int SpawnOnDeathCount;
    emitter_offset spawnOnUpdate;
    int SpawnOnUpdateCount;
};
```

GMS 2023.6.0.92
```
struct Emitter_2023_6 {
    string_offset Name;
    
    bool Enabled;   // New in 2023.6
    
    int Mode, EmitCount, Distribution, Shape;
    float RegionX, RegionY, RegionWidth, RegionHeight, Rotation;
    sprite_offset sprite;
    int Texture;
    float FrameIndex;
    bool Animate, Stretch, Random;
    uint StartColor, MidColor, EndColor;
    bool AdditiveBlend;
    float LifetimeMin, LifetimeMax,
        ScaleX, ScaleY, SizeMin, SizeMax, SizeIncrease, SizeWiggle,
        SpeedMin, SpeedMax, SpeedIncrease, SpeedWiggle,
        GravityForce, GravityDirection,
        DirectionMin, DirectionMax, DirectionIncrease, DirectionWiggle,
        OrientationMin, OrientationMax, OrientationIncrease, OrientationWiggle;
    bool OrientationRelative;
    emitter_offset spawnOnDeath;
    int SpawnOnDeathCount;
    emitter_offset spawnOnUpdate;
    int SpawnOnUpdateCount;
};
```

GMS 2023.8.0.98
```
struct Emitter_2023_8 {
    string_offset Name;
    bool Enabled;
    int Mode;
    float EmitCount;     // Changed to float in 2023.8

    // New in 2023.8
    bool EmitRelative;    // I didn't know what this was, but taking Jacky720's word for it
    float DelayMin, DelayMax;
    int DelayUnits;      // (0 = seconds, 1 = frames)
    float IntervalMin, IntervalMax;
    int IntervalUnits;   // (0 = seconds, 1 = frames);
    
    int Distribution, Shape;
    float RegionX, RegionY, RegionWidth, RegionHeight, Rotation;
    sprite_offset sprite;
    int Texture;
    float FrameIndex;
    bool Animate, Stretch, Random;
    uint StartColor, MidColor, EndColor;
    bool AdditiveBlend;
    float LifetimeMin, LifetimeMax,
        ScaleX, ScaleY, SizeMin, SizeMax, SizeIncrease, SizeWiggle,
        SpeedMin, SpeedMax, SpeedIncrease, SpeedWiggle,
        GravityForce, GravityDirection,
        DirectionMin, DirectionMax, DirectionIncrease, DirectionWiggle,
        OrientationMin, OrientationMax, OrientationIncrease, OrientationWiggle;
    bool OrientationRelative;
    emitter_offset spawnOnDeath;
    int SpawnOnDeathCount;
    emitter_offset spawnOnUpdate;
    int SpawnOnUpdateCount;
};
```
