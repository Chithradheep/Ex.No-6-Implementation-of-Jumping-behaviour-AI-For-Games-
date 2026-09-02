# Ex.No: 6  Implementation of Jumping  behaviour- Unity

### DATE:                                                                            
### REGISTER NUMBER : 2305002003

### AIM: 
To write a program to simulate the process of jumping in Unity.

### PROCEDURE:

1. Create a new 3D Unity project
2. Add a Plane
3. Right-click Hierarchy → 3D Object → Plane → Rename to Ground
4. Add a Cube (Player)
5. Right-click Hierarchy → 3D Object → Cube → Rename to Player
6. Set Position: (0, 0.5, 0)
7. Add a Rigidbody to the Player
8. With the Player selected: Inspector → Add Component → Rigidbody
9. Set Constraints > Freeze Rotation X, Z (optional for stability)
10.Create the Jump Script and Apply the Script Player
11.Run the game
Press Play
Press Spacebar to jump
Your cube should only jump when touching the ground

### PROGRAM:
```
using UnityEngine;

public class PlayerJump : MonoBehaviour
{
    private Rigidbody rb;
    public float jumpForce = 5f;
    
    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    void Update()
    {
        if (Input.GetKeyDown(KeyCode.Space) )
        {
            rb.AddForce(Vector3.up * jumpForce, ForceMode.Impulse);
            
        }
    }

   
}
```
### OUTPUT:

Before Execution:
<img width="1032" height="466" alt="image" src="https://github.com/user-attachments/assets/3fdeda5f-c4c4-4bd7-aba9-73edbc1f18c8" />

After Execution:
<img width="1031" height="475" alt="image" src="https://github.com/user-attachments/assets/0e718b75-fb9a-46ab-aaaf-e3df1ab06ff9" />


### RESULT:
Thus the simple jumping behavior was implemented successfully.
