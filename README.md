# Ryan
Melhor do momento 
using UnityEngine;

public class StealthInvisibility : MonoBehaviour
{
    public Renderer characterRenderer;
    private bool isStealing = false;

    void Update()
    {
        // Exemplo: Detecção simples de ação de roubo (tecla S como "roubar")
        if (Input.GetKeyDown(KeyCode.S))
        {
            StartStealing();
        }
        if (Input.GetKeyUp(KeyCode.S))
        {
            StopStealing();
        }
    }

    void StartStealing()
    {
        isStealing = true;
        // Deixar o personagem invisível
        characterRenderer.enabled = false;
    }

    void StopStealing()
    {
        isStealing = false;
        // Tornar o personagem visível novamente
        characterRenderer.enabled = true;
    }
}
