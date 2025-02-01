# Dragon-Breathing-Animation
Rive Animation Challenge: Dragon Breathing Animation

![Image](https://github.com/user-attachments/assets/eb2c2129-5b7a-44da-9426-2935d882da5f)

Below is the animation rive preview link
# https://rive.app/s/7b6YVfsiYEeaVB9q9rdVBg/


# Rive Animation Challenge: Dragon Breathing Animation

## Developer Documentation

Below is the code snippet used for the state machine configuration in the animation:


## Contact Information

- **Name:** Jitender Singh
- **Email:** [jitenders859@gmail.com](mailto:jitenders859@gmail.com)
- **LinkedIn:** [Jitender Singh on LinkedIn](https://www.linkedin.com/in/jitender-singh-shekhawat-549535100/)


```ts
// State Machine Inputs
interface AnimationInputs {
  smiling: boolean;         // Controls whether the character is smiling
  fireIntensity: number;      // Range: 1-100, Controls the intensity of the fire effect
  breathInProgress: number;   // Range: 1-100, Controls the progress of the breath animation
  showFire: boolean;          // Determines whether the fire is displayed
}

const artboardName = 'dragon';

// States (feel free to adjust state names to suit your animation)
enum AnimationStates {
  IDLE = 'idle',
  BREATHING = 'breathing',
  BREATHING_FIRE = 'breathingFire'
}

// Example of expected behavior with state machine configuration
interface StateMachineConfig {
  stateMachine: 'DragonControl';
  inputs: {
    smiling: {
      type: 'boolean';
      description: 'Controls whether the character is smiling';
      default: false;
    };
    fireIntensity: {
      type: 'number';
      range: [1, 100];
      description: 'Controls the intensity of the fire effect';
      default: 50;
    };
    breathInProgress: {
      type: 'number';
      range: [1, 100];
      description: 'Controls the progress of the breath animation';
      default: 0;
    };
    showFire: {
      type: 'boolean';
      description: 'Determines whether the fire is shown';
      default: false;
    };
  };
}
