# Asset OEE Smart Manufacturing Profile

This repository defines a **Smart Manufacturing Profile (SM Profile)** for publishing
asset-level Overall Equipment Effectiveness (OEE) data in a Unified Namespace (UNS).

The profile provides a **machine-readable information contract** that guarantees the
structure, types, and semantic meaning of OEE data independent of transport or platform.

## Purpose

- Enable portable analytics and applications
- Decouple data producers from data consumers
- Support CESMII Smart Manufacturing Profile

## Scope

This profile defines:
- Asset identification via logical UNS path
- Shift context (start, end, shift identifier)
- OEE components (Availability, Performance, Quality)
- Calculated overall OEE value

## Format

The profile is defined using **JSON Schema (Draft 2020-12)** and can be applied to data
published over MQTT, HTTP, OPC UA, or represented as UDTs in platforms such as Ignition.

## Files

- `schema/asset-oee-v1.schema.json`  
  The authoritative profile definition (the data contract)

- `examples/asset-oee-v1.example.json`  
  An example payload conforming to the profile

## Usage

Producers should reference the schema in published payloads using the `$schema` field.
Consumers may validate incoming payloads against the schema to ensure type safety.

## CESMII Alignment

This profile is intended to satisfy the **ProveIt Smart Manufacturing Profile requirement**
by publishing the data structure independently of the data itself, enabling reuse and
interoperability.

## License

See LICENSE file for details.
