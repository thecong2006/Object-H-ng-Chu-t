using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Gun_Mouse : MonoBehaviour
{
    void Update()
    {
        Vector3 mousePos = Input.mousePosition; //Vị trí hiện tại của chuột
        mousePos = Camera.main.ScreenToWorldPoint(mousePos); //Lấy vị trí của chuột ở Camera.main
        Vector2 dir = new Vector2(mousePos.x - transform.position.y, mousePos.y - transform.position.y);
        // phép tính để Object hướng về chuột
        transform.up = dir;
        //Object.hướng lên trên = phép tính để Object hướng về chuột
    }
}
