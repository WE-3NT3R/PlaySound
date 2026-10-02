# PlaySound

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlaySound : MonoBehaviour
{
    GameObject[] player;
    AudioSource Timmy;
    void Start()
    {
        GameObject player = GameObject.FindWithTag("Player");

        if (player != null)
            Timmy = player.GetComponent<AudioSource>();
    }

    void Update()
    {
        if (Input.GetKeyDown(KeyCode.K) && Timmy != null)
        {
            Timmy.Play();
        }
    }
}
