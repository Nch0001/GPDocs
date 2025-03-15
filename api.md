---
layout: default
title: API
nav_order: 8
description: Documentation for developers
---
# API Documentation

{: .no_toc }

Documentation for developers is currently very sparse. Please feel free to help add to this page.

## Table of Contents

{: .no_toc .text-delta}

- TOC
  {:toc}

---

# Adding GriefPrevention as a dependency

GriefPrevention will be added to maven central sometime before v20 - in the meantime, there's this neat thing called [JitPack](https://jitpack.io/#GriefPrevention/GriefPrevention) that makes a public maven repo for public Github repos on the fly.
According to it, this is all you need to do to add to your pom.xml:

## Maven

```xml
	<repositories>
		<repository>
		    <id>jitpack.io</id>
		    <url>https://jitpack.io</url>
		</repository>
	</repositories>
```

```xml
	<dependency>
	    <groupId>com.github.GriefPrevention</groupId>
	    <artifactId>GriefPrevention</artifactId>
	    <version>16.18.2</version>
            <scope>provided</scope>
	</dependency>
```

## Gradle

```gradle
repositories {
    maven {url "https://jitpack.io"}
}

dependencies {
    implementation("com.github.GriefPrevention:GriefPrevention:{GriefPrevention Version}")
}
```

You can also add it to gradle/sbt/leiningen projects: [https://jitpack.io/#GriefPrevention/GriefPrevention/](https://jitpack.io/#GriefPrevention/GriefPrevention/)

# Events

### AccrueClaimBlocksEvent

An `Event` called when a `Player` is about to recieve claim blocks

### BoundaryVisualizationEvent

An `Event` called when a `Player` recieves Boundary visuals

### ClaimChangeEvent

An `Event` called when a `Claim` is changed

### ClaimCreatedEvent

An `Event` called when a `Claim` is created

### ClaimDeletedEvent

An `Event` called when a `Claim` is deleted

### ClaimEvent

An `Event` involving a `Claim`

### ClaimExpirationEvent

An `Event` for when a [`Claim`](../Claim.html "class in com.github.GriefPrevention") is deleted due to owner inactivity.

### ClaimExtendEvent

An `Event` for when a [`Claim's`](../Claim.html "class in com.github.GriefPrevention") depth (lower Y bound) is to be extended.

### ClaimInspectionEvent

An `Event` called when a `Player` uses the claim inspection tool.

### ClaimModifiedEvent

Deprecated, for removal: This API element is subject to removal in a future version, replaced by more descriptive [`ClaimResizeEvent`](ClaimResizeEvent.html "class in com.github.GriefPrevention.events") and generic [`ClaimChangeEvent`](ClaimChangeEvent.html "class in com.github.GriefPrevention.events") An `Event` for when a [`Claim`](../Claim.html "class in com.github.GriefPrevention") is changed.

### ClaimPermissionCheckEvent

An `Event` called when a [`Claim`](../Claim.html "class in com.github.GriefPrevention") requires a specific level of trust.

### ClaimResizeEvent

An `Event` called when a [`Claim`](../Claim.html "class in com.github.GriefPrevention") is resized.

### ClaimTransferEvent

An `Event` called when a [`Claim`](../Claim.html "class in com.github.GriefPrevention") is transferred.

### MultiClaimEvent

An `Event` involving multiple [`Claims`](../Claim.html "class in com.github.GriefPrevention").

### PlayerKickBanEvent

An `Event` called when GriefPrevention kicks or bans a `Player`.

### PreventBlockBreakEvent

An `Event` called when GriefPrevention prevents a `BlockBreakEvent`.

### PreventPvPEvent

An `Event` called when GriefPrevention prevents PvP combat.

### ProtectDeathDropsEvent

An `Event` called when GriefPrevention protects items after a death.

### SaveTrappedPlayerEvent

An `Event` called when a user is rescued from a [`Claim`](../Claim.html "class in com.github.GriefPrevention").

### TrustChangedEvent

An `Event` called when a `Player` modifies [`permissions`](../ClaimPermission.html "enum class in com.github.GriefPrevention") in one or more [`claims`](../Claim.html "class in com.github.GriefPrevention").

### VisualizationEvent

Deprecated, for removal: This API element is subject to removal in a future version.Replaced with 

[`BoundaryVisualizationEvent`](BoundaryVisualizationEvent.html "class in com.github.GriefPrevention.events")---
