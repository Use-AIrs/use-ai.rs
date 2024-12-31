### Layer 1.0.0: Math

This component provides mathematical and logical operations, optimized for parallelization where possible.

- Smaller dimensions may perform better on the CPU.
- We maintain flexibility to map operations to either the GPU or CPU based on workload.

### Layer 1.1: Data Processing

#### 1.1.0: DataRawBuilder
Processes CSV files to create a `DataRaw` struct.

#### 1.1.1: DataRaw
Represents the normalized form of raw input data, making it suitable for training purposes.

#### 1.1.2: DataBuilder
Transforms a `DataRaw` instance into a `Data` structure tailored to the specific model being used.

#### 1.1.3: Data
Organizes data for training purposes, optimized for a specific model.

#### 1.1.4: Trainer
Processes a `Data` structure to produce a `DataResult`.

#### 1.1.5: DataResult
Represents the trained model.

#### 1.1.6: DataInputBuilder
Creates a `DataInput` instance from `DataRaw`, tailored to a specific model.

#### 1.1.7: DataTargetBuilder
Combines a `DataResult` with a `DataInput` to generate a `DataTarget`.

#### 1.1.8: DataTarget
Enables the generation of outputs based on a given input.

#### 1.1.9: Live (Future Feature Idea)
Plans to implement live learning capabilities in future iterations.