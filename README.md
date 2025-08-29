# Code-Blocks-Experiment-2

📡 Implementation of Go-Back-N Protocol – Selective Repeat

🎯 Aim

To write and execute a program for the Go-Back-N protocol using the Selective Repeat technique.

🛠️ Equipments Required

• 	Personal Computer

• 	Turbo C Compiler

📋 Procedure
1. 	Connect two computers in a Wired/Wireless LAN.
2. 	Ensure both computers are on the same network and can ping each other.
3. 	Open a new C file in Code::Blocks or any C IDE and type the program.
4. 	Navigate to:
Project -> Properties -> Project Build Options -> Linker Settings
Add: netproto and pthread
5. 	Execute the program on both server and client machines.
6. 	Enter the following:
• 	IP address of the remote machine
• 	Port address of both local and remote machines
• 	Error rate
7. 	Choose the file and verify the Go-Back-N protocol operation.

💻 Program

#include <stdio.h>

void main() {
    
    int i, j, n;
    printf("GO BACK N ARQ\n");
    printf("Enter number of frames: ");
    scanf("%d", &n);

    char frame[n][10];

    for (i = 1; i <= n; i++) {
        printf("Content for frame %d: ", i);
        scanf("%s", frame[i]);
    }

    printf("Enter frame number with no ACK: ");
    scanf("%d", &j);

    for (i = 1; i <= n; i++) {
        if (i != j)
            printf("\nSending frame %d\nFRAME ACKNOWLEDGED...\n", i);
    }

    if (j <= n) {
        printf("No Acknowledgement for frame %d...\n", j);
        printf("Resending... Content from frame %d: %s\n\n", j, frame[j]);
    }

    printf("\nSending frame %d\nFRAME ACKNOWLEDGED...\n", j);
    printf("\n\nALL FRAMES RECEIVED SUCCESSFULLY\n\n");
}

🖥️ Sample Output
<img width="1920" height="1080" alt="Screenshot (7)" src="https://github.com/user-attachments/assets/7ddc55ec-f1b4-4690-9a33-3af12ae86891" />
<img width="1092" height="630" alt="Screenshot 2025-08-29 085544" src="https://github.com/user-attachments/assets/112bc0df-cc71-4eaa-9b46-8d90fb394fdd" />


✅ Result

Thus, the Go-Back-N protocol using Selective Repeat was successfully implemented and verified.
